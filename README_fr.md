# Lufi pour YunoHost

[![Integration level](https://dash.yunohost.org/integration/lufi.svg)](https://dash.yunohost.org/appci/app/lufi)  
[![Install Lufi with YunoHost](https://install-app.yunohost.org/install-with-yunohost.png)](https://install-app.yunohost.org/?app=lufi)

*[Read this readme in english.](./README.md)* 

> *Ce package vous permet d'installer Lufi rapidement et simplement sur un serveur Yunohost.  
Si vous n'avez pas YunoHost, regardez [ici](https://yunohost.org/#/install) pour savoir comment l'installer et en profiter.*

## Vue d'ensemble
Il stocke vos fichiers et vous permet de les télécharger.

Est-ce tout? Non. Tous les fichiers sont cryptés par le navigateur! Non chiffré. Ça ne marche pas. L'administrateur de l'instance Lufi ne pourra pas voir quel est votre administrateur réseau ou votre FAI.

La clé de cryptage est une ancre (voir [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), ce qui signifie que cette partie n'est traitée que par le client et n'atteint pas le serveur. :-)

**Version incluse:** 0.03.5

## Captures d'écran

![](https://framalibre.org/sites/default/files/screenshot_lufi_1.png)

## Démo

* [Démo officielle](https://demo.lufi.io/)

## Configuration

Comment configurer cette application: un fichier brut en SSH.

## Documentation

 * Documentation officielle: https://framagit.org/luc/lufi/wikis/home

## Caractéristiques spécifiques YunoHost

#### Support multi-utilisateurs

L'authentification LDAP et HTTP est-elle prise en charge? **Oui**
L'application peut-elle être utilisée par plusieurs utilisateurs? **Oui**

#### Architectures supportées

* x86-64b - [![Build Status](https://ci-apps.yunohost.org/ci/logs/lufi%20%28Community%29.svg)](https://ci-apps.yunohost.org/ci/apps/lufi/)
* ARMv8-A - [![Build Status](https://ci-apps-arm.yunohost.org/ci/logs/lufi%20%28Community%29.svg)](https://ci-apps-arm.yunohost.org/ci/apps/lufi/)


## Liens

 * Signaler un bug: https://github.com/YunoHost-Apps/lufi_ynh/issues
 * Site de l'application: https://framagit.org/fiat-tux/hat-softwares/lufi
 * Dépôt de l'application principale: https://framagit.org/fiat-tux/hat-softwares/lufi
 * Site web YunoHost: https://yunohost.org/

---

Informations pour les développeurs
----------------

**Seulement si vous voulez utiliser une branche de test pour le codage, au lieu de fusionner directement dans la banche principale.**
Merci de faire vos pull request sur la [branche testing](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

Pour essayer la branche testing, procédez comme suit.
```
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
ou
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**Plus d'informations sur la page de documentation:**  
https://yunohost.org/packaging_apps

# Lufi for YunoHost

[![Latest Version](https://img.shields.io/badge/version-_--_-green.svg?style=flat)](https://github.com/YunoHost-Apps/lufi_ynh/releases)
[![Status](https://img.shields.io/badge/status-working-yellow.svg?style=flat)](https://github.com/YunoHost-Apps/lufi_ynh/milestones)
[![Dependencies](https://img.shields.io/badge/dependencies-includes-lightgrey.svg?style=flat)](https://github.com/YunoHost-Apps/lufi_ynh#dependencies)
[![GitHub license](https://img.shields.io/badge/license-GPLv3-blue.svg?style=flat)](https://raw.githubusercontent.com/YunoHost-Apps/lufi_ynh/master/LICENSE)
[![Yunohost version](https://img.shields.io/badge/yunohost-2.4.2_tested-orange.svg?style=flat)](https://github.com/YunoHost/yunohost)
[![GitHub issues](https://img.shields.io/github/issues/YunoHost-Apps/lufi_ynh.svg?style=flat)](https://github.com/YunoHost-Apps/lufi_ynh/issues)

## Lufi c'est quoi ?

Il stocke vos fichiers et vous permet de les télécharger.

Est-ce tout? Non. Tous les fichiers sont cryptés par le navigateur! Non chiffré. Ça ne marche pas. L'administrateur de l'instance Lufi ne pourra pas voir quel est votre administrateur réseau ou votre FAI.

La clé de cryptage est une ancre (voir Fragment Identifier), ce qui signifie que cette partie n'est traitée que par le client et n'atteint pas le serveur. :-)

Source: [Documentation de Lufi](https://framagit.org/luc/lufi/wikis/home)

### Installation

`$ sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh.git`

### Mise à jour

`$ sudo yunohost app upgrade --verbose lufi -u https://github.com/YunoHost-Apps/lufi_ynh.git`

## What is Lufi?

It stores files and allows you to download them.

Is that all? No. All the files are encrypted by the browser! It means that your files never leave your computer unencrypted. The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.

The encryption key part of the URL is a anchor (Cf. Fragment Identifier), that means this part is only processed client-side and does not reach the server. :-)

Source: [Lufi documentation](https://framagit.org/luc/lufi/wikis/home)

### Install

`$ sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh.git`

### Update

`$ sudo yunohost app upgrade --verbose lufi -u https://github.com/YunoHost-Apps/lufi_ynh.git`
