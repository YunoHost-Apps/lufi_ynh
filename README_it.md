<!--
N.B.: Questo README è stato automaticamente generato da <https://github.com/YunoHost/apps/tree/master/tools/readme_generator>
NON DEVE essere modificato manualmente.
-->

# Lufi per YunoHost

[![Livello di integrazione](https://dash.yunohost.org/integration/lufi.svg)](https://dash.yunohost.org/appci/app/lufi) ![Stato di funzionamento](https://ci-apps.yunohost.org/ci/badges/lufi.status.svg) ![Stato di manutenzione](https://ci-apps.yunohost.org/ci/badges/lufi.maintain.svg)

[![Installa Lufi con YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=lufi)

*[Leggi questo README in altre lingue.](./ALL_README.md)*

> *Questo pacchetto ti permette di installare Lufi su un server YunoHost in modo semplice e veloce.*  
> *Se non hai YunoHost, consulta [la guida](https://yunohost.org/install) per imparare a installarlo.*

## Panoramica

Lufi stores files and allows you to download them. Is that all? No. All the files are encrypted **by the browser**! It means that your files **never** leave your computer unencrypted.
The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.
The encryption key part of the URL is a anchor (Cf. [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), that means this part is only processed client-side and does not reach the server. :-)


**Versione pubblicata:** 0.05.21~ynh2

**Prova:** <https://demo.lufi.io/>

## Screenshot

![Screenshot di Lufi](./doc/screenshots/screenshot_lufi_1.png)

## Documentazione e risorse

- Sito web ufficiale dell’app: <https://git.framasoft.org/luc/lufi>
- Documentazione ufficiale per gli amministratori: <https://framagit.org/luc/lufi/wikis/home>
- Repository upstream del codice dell’app: <https://framagit.org/fiat-tux/hat-softwares/lufi>
- Store di YunoHost: <https://apps.yunohost.org/app/lufi>
- Segnala un problema: <https://github.com/YunoHost-Apps/lufi_ynh/issues>

## Informazioni per sviluppatori

Si prega di inviare la tua pull request alla [branch di `testing`](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

Per provare la branch di `testing`, si prega di procedere in questo modo:

```bash
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
o
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**Maggiori informazioni riguardo il pacchetto di quest’app:** <https://yunohost.org/packaging_apps>
