<!--
N.B.: README ini dibuat secara otomatis oleh <https://github.com/YunoHost/apps/tree/master/tools/readme_generator>
Ini TIDAK boleh diedit dengan tangan.
-->

# Lufi untuk YunoHost

[![Tingkat integrasi](https://dash.yunohost.org/integration/lufi.svg)](https://ci-apps.yunohost.org/ci/apps/lufi/) ![Status kerja](https://ci-apps.yunohost.org/ci/badges/lufi.status.svg) ![Status pemeliharaan](https://ci-apps.yunohost.org/ci/badges/lufi.maintain.svg)

[![Pasang Lufi dengan YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=lufi)

*[Baca README ini dengan bahasa yang lain.](./ALL_README.md)*

> *Paket ini memperbolehkan Anda untuk memasang Lufi secara cepat dan mudah pada server YunoHost.*  
> *Bila Anda tidak mempunyai YunoHost, silakan berkonsultasi dengan [panduan](https://yunohost.org/install) untuk mempelajari bagaimana untuk memasangnya.*

## Ringkasan

Lufi stores files and allows you to download them. Is that all? No. All the files are encrypted **by the browser**! It means that your files **never** leave your computer unencrypted.
The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.
The encryption key part of the URL is a anchor (Cf. [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), that means this part is only processed client-side and does not reach the server. :-)


**Versi terkirim:** 0.07.0~ynh1

**Demo:** <https://demo.lufi.io/>

## Tangkapan Layar

![Tangkapan Layar pada Lufi](./doc/screenshots/screenshot_lufi_1.png)

## Dokumentasi dan sumber daya

- Website aplikasi resmi: <https://git.framasoft.org/luc/lufi>
- Dokumentasi admin resmi: <https://framagit.org/luc/lufi/wikis/home>
- Depot kode aplikasi hulu: <https://framagit.org/fiat-tux/hat-softwares/lufi>
- Gudang YunoHost: <https://apps.yunohost.org/app/lufi>
- Laporkan bug: <https://github.com/YunoHost-Apps/lufi_ynh/issues>

## Info developer

Silakan kirim pull request ke [`testing` branch](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

Untuk mencoba branch `testing`, silakan dilanjutkan seperti:

```bash
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
atau
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**Info lebih lanjut mengenai pemaketan aplikasi:** <https://yunohost.org/packaging_apps>
