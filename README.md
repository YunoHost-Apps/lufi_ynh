# Lufi for YunoHost

[![Integration level](https://dash.yunohost.org/integration/lufi.svg)](https://dash.yunohost.org/appci/app/lufi)  
[![Install Lufi with YunoHost](https://install-app.yunohost.org/install-with-yunohost.png)](https://install-app.yunohost.org/?app=lufi)

*[Lire ce readme en français.](./README_fr.md)*

> *This package allow you to install Lufi quickly and simply on a YunoHost server.  
If you don't have YunoHost, please see [here](https://yunohost.org/#/install) to know how to install and enjoy it.*

## Overview
It stores files and allows you to download them.

Is that all? No. All the files are encrypted **by the browser**! It means that your files **never** leave your computer unencrypted.
The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.

The encryption key part of the URL is a anchor (Cf. [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), that means this part is only processed client-side and does not reach the server. :-)

**Shipped version:** 0.04.6

## Screenshots

![](https://framalibre.org/sites/default/files/screenshot_lufi_1.png)

## Demo

* [Official demo](https://demo.lufi.io/)

## Configuration

How to configure this app: a plain file with SSH.

## Documentation

 * Official documentation: https://framagit.org/luc/lufi/wikis/home

## YunoHost specific features

#### Multi-users support

Are LDAP and HTTP auth supported? **Yes**
Can the app be used by multiple users? **Yes**

#### Supported architectures

* x86-64b - [![Build Status](https://ci-apps.yunohost.org/ci/logs/lufi%20%28Community%29.svg)](https://ci-apps.yunohost.org/ci/apps/lufi/)
* ARMv8-A - [![Build Status](https://ci-apps-arm.yunohost.org/ci/logs/lufi%20%28Community%29.svg)](https://ci-apps-arm.yunohost.org/ci/apps/lufi/)

## Links

 * Report a bug: https://github.com/YunoHost-Apps/lufi_ynh/issues
 * App website: https://framagit.org/fiat-tux/hat-softwares/lufi
 * Upstream app repository: https://framagit.org/fiat-tux/hat-softwares/lufi
 * YunoHost website: https://yunohost.org/

---

Developers info
----------------

**Only if you want to use a testing branch for coding, instead of merging directly into master.**
Please do your pull request to the [testing branch](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

To try the testing branch, please proceed like that.
```
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
or
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**More information on the documentation page:**  
https://yunohost.org/packaging_apps
