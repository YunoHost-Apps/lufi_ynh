<!--
Важно: этот README был автоматически сгенерирован <https://github.com/YunoHost/apps/tree/master/tools/readme_generator>
Он НЕ ДОЛЖЕН редактироваться вручную.
-->

# Lufi для YunoHost

[![Уровень интеграции](https://apps.yunohost.org/badge/integration/lufi)](https://ci-apps.yunohost.org/ci/apps/lufi/)
![Состояние работы](https://apps.yunohost.org/badge/state/lufi)
![Состояние сопровождения](https://apps.yunohost.org/badge/maintained/lufi)

[![Установите Lufi с YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=lufi)

*[Прочтите этот README на других языках.](./ALL_README.md)*

> *Этот пакет позволяет Вам установить Lufi быстро и просто на YunoHost-сервер.*  
> *Если у Вас нет YunoHost, пожалуйста, посмотрите [инструкцию](https://yunohost.org/install), чтобы узнать, как установить его.*

## Обзор

Lufi stores files and allows you to download them. Is that all? No. All the files are encrypted **by the browser**! It means that your files **never** leave your computer unencrypted.
The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.
The encryption key part of the URL is a anchor (Cf. [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), that means this part is only processed client-side and does not reach the server. :-)


**Поставляемая версия:** 0.07.0~ynh2

**Демо-версия:** <https://demo.lufi.io/>

## Снимки экрана

![Снимок экрана Lufi](./doc/screenshots/screenshot_lufi_1.png)

## Документация и ресурсы

- Официальный веб-сайт приложения: <https://git.framasoft.org/luc/lufi>
- Официальная документация администратора: <https://framagit.org/luc/lufi/wikis/home>
- Репозиторий кода главной ветки приложения: <https://framagit.org/fiat-tux/hat-softwares/lufi>
- Магазин YunoHost: <https://apps.yunohost.org/app/lufi>
- Сообщите об ошибке: <https://github.com/YunoHost-Apps/lufi_ynh/issues>

## Информация для разработчиков

Пришлите Ваш запрос на слияние в [ветку `testing`](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing).

Чтобы попробовать ветку `testing`, пожалуйста, сделайте что-то вроде этого:

```bash
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
или
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**Больше информации о пакетировании приложений:** <https://yunohost.org/packaging_apps>
