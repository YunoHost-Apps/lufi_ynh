<!--
NB: Deze README is automatisch gegenereerd door <https://github.com/YunoHost/apps/tree/master/tools/readme_generator>
Hij mag NIET handmatig aangepast worden.
-->

# Lufi voor Yunohost

[![Integratieniveau](https://apps.yunohost.org/badge/integration/lufi)](https://ci-apps.yunohost.org/ci/apps/lufi/)
![Mate van functioneren](https://apps.yunohost.org/badge/state/lufi)
![Onderhoudsstatus](https://apps.yunohost.org/badge/maintained/lufi)

[![Lufi met Yunohost installeren](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=lufi)

*[Deze README in een andere taal lezen.](./ALL_README.md)*

> *Met dit pakket kun je Lufi snel en eenvoudig op een YunoHost-server installeren.*  
> *Als je nog geen YunoHost hebt, lees dan [de installatiehandleiding](https://yunohost.org/install), om te zien hoe je 'm installeert.*

## Overzicht

Lufi stores files and allows you to download them. Is that all? No. All the files are encrypted **by the browser**! It means that your files **never** leave your computer unencrypted.
The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.
The encryption key part of the URL is a anchor (Cf. [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), that means this part is only processed client-side and does not reach the server. :-)


**Geleverde versie:** 0.07.0~ynh2

**Demo:** <https://demo.lufi.io/>

## Schermafdrukken

![Schermafdrukken van Lufi](./doc/screenshots/screenshot_lufi_1.png)

## Documentatie en bronnen

- Officiele website van de app: <https://git.framasoft.org/luc/lufi>
- Officiele beheerdersdocumentatie: <https://framagit.org/luc/lufi/wikis/home>
- Upstream app codedepot: <https://framagit.org/fiat-tux/hat-softwares/lufi>
- YunoHost-store: <https://apps.yunohost.org/app/lufi>
- Meld een bug: <https://github.com/YunoHost-Apps/lufi_ynh/issues>

## Ontwikkelaarsinformatie

Stuur je pull request alsjeblieft naar de [`testing`-branch](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

Om de `testing`-branch uit te proberen, ga als volgt te werk:

```bash
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
of
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**Verdere informatie over app-packaging:** <https://yunohost.org/packaging_apps>
