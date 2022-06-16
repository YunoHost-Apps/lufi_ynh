# Lufi pour YunoHost

[![Niveau d'intégration](https://dash.yunohost.org/integration/lufi.svg)](https://dash.yunohost.org/appci/app/lufi) ![](https://ci-apps.yunohost.org/ci/badges/lufi.status.svg) ![](https://ci-apps.yunohost.org/ci/badges/lufi.maintain.svg)  
[![Installer Lufi avec YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=lufi)

*[Read this readme in english.](./README.md)*
*[Lire ce readme en français.](./README_fr.md)*

> *Ce package vous permet d'installer Lufi rapidement et simplement sur un serveur YunoHost.
Si vous n'avez pas YunoHost, regardez [ici](https://yunohost.org/#/install) pour savoir comment l'installer et en profiter.*

## Vue d'ensemble

It stores files and allows you to download them.

Is that all? No. All the files are encrypted **by the browser**! It means that your files **never** leave your computer unencrypted.
The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.

The encryption key part of the URL is a anchor (Cf. [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), that means this part is only processed client-side and does not reach the server. :-)


**Version incluse :** 0.05.18~ynh1

**Démo :** https://demo.lufi.io/

## Captures d'écran

![](./doc/screenshots/screenshot_lufi_1.png)

## Avertissements / informations importantes

## Configuration

* Comment configurer cette application: un fichier brut `/var/www/lufi/lufi.conf` en SSH.

## Documentations et ressources

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