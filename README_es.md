<!--
Este archivo README esta generado automaticamente<https://github.com/YunoHost/apps/tree/master/tools/readme_generator>
No se debe editar a mano.
-->

# Lufi para Yunohost

[![Nivel de integración](https://apps.yunohost.org/badge/integration/lufi)](https://ci-apps.yunohost.org/ci/apps/lufi/)
![Estado funcional](https://apps.yunohost.org/badge/state/lufi)
![Estado En Mantención](https://apps.yunohost.org/badge/maintained/lufi)

[![Instalar Lufi con Yunhost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=lufi)

*[Leer este README en otros idiomas.](./ALL_README.md)*

> *Este paquete le permite instalarLufi rapidamente y simplement en un servidor YunoHost.*  
> *Si no tiene YunoHost, visita [the guide](https://yunohost.org/install) para aprender como instalarla.*

## Descripción general

Lufi stores files and allows you to download them. Is that all? No. All the files are encrypted **by the browser**! It means that your files **never** leave your computer unencrypted.
The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.
The encryption key part of the URL is a anchor (Cf. [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), that means this part is only processed client-side and does not reach the server. :-)


**Versión actual:** 0.07.0~ynh2

**Demo:** <https://demo.lufi.io/>

## Capturas

![Captura de Lufi](./doc/screenshots/screenshot_lufi_1.png)

## Documentaciones y recursos

- Sitio web oficial: <https://git.framasoft.org/luc/lufi>
- Documentación administrador oficial: <https://framagit.org/luc/lufi/wikis/home>
- Repositorio del código fuente oficial de la aplicación : <https://framagit.org/fiat-tux/hat-softwares/lufi>
- Catálogo YunoHost: <https://apps.yunohost.org/app/lufi>
- Reportar un error: <https://github.com/YunoHost-Apps/lufi_ynh/issues>

## Información para desarrolladores

Por favor enviar sus correcciones a la [rama `testing`](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

Para probar la rama `testing`, sigue asÍ:

```bash
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
o
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**Mas informaciones sobre el empaquetado de aplicaciones:** <https://yunohost.org/packaging_apps>
