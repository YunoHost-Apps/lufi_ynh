#!/bin/bash

ynh_version="2.5"

YNH_VERSION () {	# Returns the version number of the Yunohost moulinette
	ynh_version=$(sudo yunohost -v | grep "moulinette:" | cut -d' ' -f2 | cut -d'.' -f1,2)
}

CHECK_VAR () {	# Verifies that the variable is not empty.
	# $1 = Variable to be checked
	# $2 = Display text on error
	test -n "$1" || (echo "$2" >&2 && false)
}

EXIT_PROPERLY () {	# Causes the script to stop in the event of an error. And clean the residue.
	trap '' ERR
	echo -e "\e[91m \e[1m"	# Shell in light red bold
	echo -e "!!\n  $app install's script has encountered an error. Installation was cancelled.\n!!" >&2

	if type -t CLEAN_SETUP > /dev/null; then	# Checks the existence of the function before executing it.
		CLEAN_SETUP	# Call the specific cleanup function of the install script.
	fi

	# Compensates the ssowat bug that does not remove the app's input in case of installation error.
	sudo sed -i "\@\"$domain$path/\":@d" /etc/ssowat/conf.json

	if [ "$ynh_version" = "2.2" ]; then
		/bin/bash $script_dir/remove
	fi

	ynh_die
}

TRAP_ON () {	# Activate signal capture
	trap EXIT_PROPERLY ERR	# Capturing exit signals on error
}

TRAP_OFF () {	# Ignoring signal capture until TRAP_ON
	trap '' ERR	# Ignoring exit signals
}

CHECK_USER () {	# Check the validity of the user admin
	# $1 = User admin variable
	ynh_user_exists "$1" || (echo "Wrong admin" >&2 && false)
}

CHECK_PATH () {	# Checks / at the beginning of the path. And his absence at the end.
	if [ "${path:0:1}" != "/" ]; then    # If the first character is not /
		path="/$path"    # Add / at the beginning of path
	fi
	if [ "${path:${#path}-1}" == "/" ] && [ ${#path} -gt 1 ]; then    # If the last character is a / and it is not the only character.
		path="${path:0:${#path}-1}"	# Delete last character
	fi
}

CHECK_DOMAINPATH () {	# Checks the availability of the path and domain.
	sudo yunohost app checkurl $domain$path -a $app
}

CHECK_FINALPATH () {	# Checks that the destination folder is not already in use.
	final_path=/var/www/$app
	if [ -e "$final_path" ]
	then
		echo "This path already contains a folder" >&2
		false
	fi
}

SETUP_SOURCE () {	# Download source, decompress and copu into $final_path
	src=$(cat ../sources/source_md5 | awk -F' ' {'print $2'})
	sudo wget -nv -i ../sources/source_url -O $src
	# Checks the checksum of the downloaded source.
	md5sum -c ../sources/source_md5 --status || ynh_die "Corrupt source"
	# Decompress source
	if [ "$(echo ${src##*.})" == "tgz" ]; then
		tar -x -f $src
	elif [ "$(echo ${src##*.})" == "zip" ]; then
		unzip -q $src
	else
		false	# Unsupported archive format.
	fi
	# Copy file source
	sudo cp -a $(cat ../sources/source_dir)/. "$final_path"
	# Copy additional file and modified
	if test -e "../sources/ajouts"; then
		sudo cp -a ../sources/ajouts/. "$final_path"
	fi
}

ADD_SYS_USER () {   # Créer un utilisateur système dédié à l'app
        if ! ynh_system_user_exists "$app"	# Test l'existence de l'utilisateur
        then
            sudo useradd -d /var/www/$app --system --user-group $app --shell /usr/sbin/nologin || (echo "Unable to create $app system account" >&2 && false)
        fi
}

STORE_MD5_CONFIG () {	# Saves the checksum of the config file
	# $1 = Name of the conf file for storage in settings.yml
	# $2 = Full name and path of the conf file.
	ynh_app_setting_set $app $1_file_md5 $(sudo md5sum "$2" | cut -d' ' -f1)
}

CHECK_MD5_CONFIG () {	# Created a backup of the config file if it was changed.
	# $1 = Name of the conf file for storage in settings.yml
	# $2 = Full name and path of the conf file.onf.
	if [ "$(ynh_app_setting_get $app $1_file_md5)" != $(sudo md5sum "$2" | cut -d' ' -f1) ]; then
		sudo cp -a "$2" "$2.backup.$(date '+%d.%m.%y_%Hh%M,%Ss')"	# Si le fichier de config a été modifié, créer un backup.
	fi
}

### REMOVE SCRIPT

REMOVE_NGINX_CONF () {	# Delete nginx configuration
	if [ -e "/etc/nginx/conf.d/$domain.d/$app.conf" ]; then	# Delete nginx config
		echo "Delete nginx config"
		sudo rm "/etc/nginx/conf.d/$domain.d/$app.conf"
		sudo service nginx reload
	fi
}

REMOVE_LOGROTATE_CONF () {	# Delete logrotate configuration
	if [ -e "/etc/logrotate.d/$app" ]; then
		echo "Delete logrotate config"
		sudo rm "/etc/logrotate.d/$app"
	fi
}

SECURE_REMOVE () {      # Deleting a folder with variable verification
	chaine="$1"	# The argument must be given between simple quotes '', to avoid interpreting the variables.
	no_var=0
	while (echo "$chaine" | grep -q '\$')	# Loop as long as there are $ in the string
	do
		no_var=1
		global_var=$(echo "$chaine" | cut -d '$' -f 2)	# Isole the first variable found.
		only_var=\$$(expr "$global_var" : '\([A-Za-z0-9_]*\)')	# Isole completely the variable by adding the $ at the beginning and keeping only the name of the variable. Mostly gets rid of / and a possible path behind.
		real_var=$(eval "echo ${only_var}")		# `eval "echo ${var}` Allows to interpret a variable contained in a variable.
		if test -z "$real_var" || [ "$real_var" = "/" ]; then
			echo "Variable $only_var is empty, suppression of $chaine cancelled." >&2
			return 1
		fi
		chaine=$(echo "$chaine" | sed "s@$only_var@$real_var@")	# Replaces variable with its value in the string.
	done
	if [ "$no_var" -eq 1 ]
	then
		if [ -e "$chaine" ]; then
			echo "Delete directory $chaine"
			sudo rm -r "$chaine"
		fi
		return 0
	else
		echo "No detected variable." >&2
		return 1
	fi
}

REMOVE_SYS_USER () {   # Delete user 
    if ynh_system_user_exists "$app"	# Test user exist
    then
    	sudo userdel $app
    fi
}

# Find a free port and return it
#
# example: port=$(ynh_find_port 8080)
#
# usage: ynh_find_port begin_port
# | arg: begin_port - port to start to search
ynh_find_port () {
	port=$1
	test -n "$port" || ynh_die "The argument of ynh_find_port must be a valid port."
	while netcat -z 127.0.0.1 $port       # Check if the port is free
	do
		port=$((port+1))	# Else, pass to next port
	done
	echo $port
}

#=================================================
# BACKUP
#=================================================

# Manage a fail of the script
#
# Print a warning to inform that the script was failed
# Execute the ynh_clean_setup function if used in the app script
#
# usage of ynh_clean_setup function
# This function provide a way to clean some residual of installation that not managed by remove script.
# To use it, simply add in your script:
# ynh_clean_setup () {
#        instructions...
# }
# This function is optionnal.
#
# Usage: ynh_exit_properly is used only by the helper ynh_check_error.
# You must not use it directly.
ynh_exit_properly () {
	exit_code=$?
	if [ "$exit_code" -eq 0 ]; then
			ynh_die	# Exit without error if the script ended correctly
	fi

	trap '' EXIT	# Ignore new exit signals
	set +eu	# Do not exit anymore if a command fail or if a variable is empty

	echo -e "!!\n  $app's script has encountered an error. Its execution was cancelled.\n!!" >&2

	if type -t ynh_clean_setup > /dev/null; then	# Check if the function exist in the app script.
		ynh_clean_setup	# Call the function to do specific cleaning for the app.
	fi

	ynh_die	# Exit with error status
}

# Exit if an error occurs during the execution of the script.
#
# Stop immediatly the execution if an error occured or if a empty variable is used.
# The execution of the script is derivate to ynh_exit_properly function before exit.
#
# Usage: ynh_abort_if_errors
ynh_abort_if_errors () {
	set -eu	# Exit if a command fail, and if a variable is used unset.
	trap ynh_exit_properly EXIT	# Capturing exit signals on shell script
}
