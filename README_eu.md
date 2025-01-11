<!--
Ohart ongi: README hau automatikoki sortu da <https://github.com/YunoHost/apps/tree/master/tools/readme_generator>ri esker
EZ editatu eskuz.
-->

# Lufi YunoHost-erako

[![Integrazio maila](https://dash.yunohost.org/integration/lufi.svg)](https://ci-apps.yunohost.org/ci/apps/lufi/) ![Funtzionamendu egoera](https://ci-apps.yunohost.org/ci/badges/lufi.status.svg) ![Mantentze egoera](https://ci-apps.yunohost.org/ci/badges/lufi.maintain.svg)

[![Instalatu Lufi YunoHost-ekin](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=lufi)

*[Irakurri README hau beste hizkuntzatan.](./ALL_README.md)*

> *Pakete honek Lufi YunoHost zerbitzari batean azkar eta zailtasunik gabe instalatzea ahalbidetzen dizu.*  
> *YunoHost ez baduzu, kontsultatu [gida](https://yunohost.org/install) nola instalatu ikasteko.*

## Aurreikuspena

Lufi stores files and allows you to download them. Is that all? No. All the files are encrypted **by the browser**! It means that your files **never** leave your computer unencrypted.
The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.
The encryption key part of the URL is a anchor (Cf. [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), that means this part is only processed client-side and does not reach the server. :-)


**Paketatutako bertsioa:** 0.07.0~ynh1

**Demoa:** <https://demo.lufi.io/>

## Pantaila-argazkiak

![Lufi(r)en pantaila-argazkia](./doc/screenshots/screenshot_lufi_1.png)

## Dokumentazioa eta baliabideak

- Aplikazioaren webgune ofiziala: <https://git.framasoft.org/luc/lufi>
- Administratzaileen dokumentazio ofiziala: <https://framagit.org/luc/lufi/wikis/home>
- Jatorrizko aplikazioaren kode-gordailua: <https://framagit.org/fiat-tux/hat-softwares/lufi>
- YunoHost Denda: <https://apps.yunohost.org/app/lufi>
- Eman errore baten berri: <https://github.com/YunoHost-Apps/lufi_ynh/issues>

## Garatzaileentzako informazioa

Bidali `pull request`a [`testing` abarrera](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

`testing` abarra probatzeko, ondorengoa egin:

```bash
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
edo
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**Informazio gehiago aplikazioaren paketatzeari buruz:** <https://yunohost.org/packaging_apps>
