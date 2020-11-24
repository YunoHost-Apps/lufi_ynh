# Lufi pour YunoHost

[![Niveau d'intégration](https://dash.yunohost.org/integration/lufi.svg)](https://dash.yunohost.org/appci/app/lufi) ![](https://ci-apps.yunohost.org/ci/badges/lufi.status.svg) ![](https://ci-apps.yunohost.org/ci/badges/lufi.maintain.svg)  
[![Installer Lufi avec YunoHost](https://install-app.yunohost.org/install-with-yunohost.png)](https://install-app.yunohost.org/?app=lufi)

*[Read this readme in english.](./README.md)* 

> *Ce package vous permet d'installer Lufi rapidement et simplement sur un serveur YunoHost.  
Si vous n'avez pas YunoHost, consultez [le guide](https://yunohost.org/#/install) pour apprendre comment l'installer.*

## Vue d'ensemble
Il stocke vos fichiers et vous permet de les télécharger.

Est-ce tout ? Non. Tous les fichiers sont chiffrés par le navigateur ! L'administrateur de l'instance Lufi ne pourra pas voir quel est votre administrateur réseau ou votre FAI.

La clé de déchiffrement est une ancre (voir [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), ce qui signifie que cette partie n'est traitée que par le client et n'atteint pas le serveur. :-)

**Version incluse:** 0.05.7

## Captures d'écran

![](https://framalibre.org/sites/default/files/screenshot_lufi_1.png)

## Démo

* [Démo officielle](https://demo.lufi.io/)

## Configuration

* Comment configurer cette application: un fichier brut `/var/www/lufi/lufi.conf`  en SSH.

## Documentation

 * Documentation officielle : https://framagit.org/luc/lufi/wikis/home
 * Documentation YunoHost : https://yunohost.org/#/app_lufi_fr

## Caractéristiques spécifiques YunoHost

#### Support multi-utilisateur

* L'authentification LDAP et HTTP est-elle prise en charge ? **Oui**
* L'application peut-elle être utilisée par plusieurs utilisateurs ? **Oui**

#### Architectures supportées

* x86-64 - [![Build Status](https://ci-apps.yunohost.org/ci/logs/lufi%20%28Apps%29.svg)](https://ci-apps.yunohost.org/ci/apps/lufi/)
* ARMv8-A - [![Build Status](https://ci-apps-arm.yunohost.org/ci/logs/lufi%20%28Apps%29.svg)](https://ci-apps-arm.yunohost.org/ci/apps/lufi/)

## Liens

 * Signaler un bug : https://github.com/YunoHost-Apps/lufi_ynh/issues
 * Dépôt de l'application principale : https://framagit.org/fiat-tux/hat-softwares/lufi
 * Site web YunoHost : https://yunohost.org/

---

## Informations pour les développeurs

Merci de faire vos pull request sur la [branche testing](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

Pour essayer la branche testing, procédez comme suit.
```
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
ou
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```
