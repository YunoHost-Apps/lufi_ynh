# Lufi pour YunoHost

[![Niveau d'intégration](https://dash.yunohost.org/integration/lufi.svg)](https://dash.yunohost.org/appci/app/lufi) ![](https://ci-apps.yunohost.org/ci/badges/lufi.status.svg) ![](https://ci-apps.yunohost.org/ci/badges/lufi.maintain.svg)  
[![Installer Lufi avec YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=lufi)

*[Read this readme in english.](./README.md)*
*[Lire ce readme en français.](./README_fr.md)*

> *Ce package vous permet d'installer Lufi rapidement et simplement sur un serveur YunoHost.
Si vous n'avez pas YunoHost, regardez [ici](https://yunohost.org/#/install) pour savoir comment l'installer et en profiter.*

## Vue d'ensemble

Application d'hébergement et de partage de fichiers anonyme

**Version incluse :** 0.05.14~ynh1

**Démo :** https://demo.lufi.io/

## Captures d'écran

![](./doc/screenshots/screenshot_lufi_1.png)

## Avertissements / informations importantes

## Configuration

* Comment configurer cette application: un fichier brut `/var/www/lufi/lufi.conf` en SSH.

## Documentations et ressources

* Site officiel de l'app : https://example.com
* Documentation officielle utilisateur : https://yunohost.org/en/app_lufi
* Documentation officielle de l'admin : https://framagit.org/luc/lufi/wikis/home
* Dépôt de code officiel de l'app : https://framagit.org/fiat-tux/hat-softwares/lufi
* Documentation YunoHost pour cette app : https://yunohost.org/app_lufi
* Signaler un bug : https://github.com/YunoHost-Apps/lufi_ynh/issues

## Informations pour les développeurs

Merci de faire vos pull request sur la [branche testing](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

Pour essayer la branche testing, procédez comme suit.
```
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
ou
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**Plus d'infos sur le packaging d'applications :** https://yunohost.org/packaging_apps