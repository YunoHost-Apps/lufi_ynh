<!--
NOTA: Este README foi creado automáticamente por <https://github.com/YunoHost/apps/tree/master/tools/readme_generator>
NON debe editarse manualmente.
-->

# Lufi para YunoHost

[![Nivel de integración](https://apps.yunohost.org/badge/integration/lufi)](https://ci-apps.yunohost.org/ci/apps/lufi/)
![Estado de funcionamento](https://apps.yunohost.org/badge/state/lufi)
![Estado de mantemento](https://apps.yunohost.org/badge/maintained/lufi)

[![Instalar Lufi con YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=lufi)

*[Le este README en outros idiomas.](./ALL_README.md)*

> *Este paquete permíteche instalar Lufi de xeito rápido e doado nun servidor YunoHost.*  
> *Se non usas YunoHost, le a [documentación](https://yunohost.org/install) para saber como instalalo.*

## Vista xeral

Lufi stores files and allows you to download them. Is that all? No. All the files are encrypted **by the browser**! It means that your files **never** leave your computer unencrypted.
The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.
The encryption key part of the URL is a anchor (Cf. [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), that means this part is only processed client-side and does not reach the server. :-)


**Versión proporcionada:** 0.07.0~ynh2

**Demo:** <https://demo.lufi.io/>

## Capturas de pantalla

![Captura de pantalla de Lufi](./doc/screenshots/screenshot_lufi_1.png)

## Documentación e recursos

- Web oficial da app: <https://git.framasoft.org/luc/lufi>
- Documentación oficial para admin: <https://framagit.org/luc/lufi/wikis/home>
- Repositorio de orixe do código: <https://framagit.org/fiat-tux/hat-softwares/lufi>
- Tenda YunoHost: <https://apps.yunohost.org/app/lufi>
- Informar dun problema: <https://github.com/YunoHost-Apps/lufi_ynh/issues>

## Info de desenvolvemento

Envía a túa colaboración á [rama `testing`](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

Para probar a rama `testing`, procede deste xeito:

```bash
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
ou
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**Máis info sobre o empaquetado da app:** <https://yunohost.org/packaging_apps>
