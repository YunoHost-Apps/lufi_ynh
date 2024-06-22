<!--
注意：此 README 由 <https://github.com/YunoHost/apps/tree/master/tools/readme_generator> 自动生成
请勿手动编辑。
-->

# YunoHost 上的 Lufi

[![集成程度](https://dash.yunohost.org/integration/lufi.svg)](https://dash.yunohost.org/appci/app/lufi) ![工作状态](https://ci-apps.yunohost.org/ci/badges/lufi.status.svg) ![维护状态](https://ci-apps.yunohost.org/ci/badges/lufi.maintain.svg)

[![使用 YunoHost 安装 Lufi](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=lufi)

*[阅读此 README 的其它语言版本。](./ALL_README.md)*

> *通过此软件包，您可以在 YunoHost 服务器上快速、简单地安装 Lufi。*  
> *如果您还没有 YunoHost，请参阅[指南](https://yunohost.org/install)了解如何安装它。*

## 概况

Lufi stores files and allows you to download them. Is that all? No. All the files are encrypted **by the browser**! It means that your files **never** leave your computer unencrypted.
The administrator of the Lufi instance you use will not be able to see what is in your file, neither will your network administrator, or your ISP.
The encryption key part of the URL is a anchor (Cf. [Fragment Identifier](https://en.wikipedia.org/wiki/Fragment_identifier)), that means this part is only processed client-side and does not reach the server. :-)


**分发版本：** 0.07.0~ynh1

**演示：** <https://demo.lufi.io/>

## 截图

![Lufi 的截图](./doc/screenshots/screenshot_lufi_1.png)

## 文档与资源

- 官方应用网站： <https://git.framasoft.org/luc/lufi>
- 官方管理文档： <https://framagit.org/luc/lufi/wikis/home>
- 上游应用代码库： <https://framagit.org/fiat-tux/hat-softwares/lufi>
- YunoHost 商店： <https://apps.yunohost.org/app/lufi>
- 报告 bug： <https://github.com/YunoHost-Apps/lufi_ynh/issues>

## 开发者信息

请向 [`testing` 分支](https://github.com/YunoHost-Apps/lufi_ynh/tree/testing) 发送拉取请求。

如要尝试 `testing` 分支，请这样操作：

```bash
sudo yunohost app install https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
或
sudo yunohost app upgrade lufi -u https://github.com/YunoHost-Apps/lufi_ynh/tree/testing --debug
```

**有关应用打包的更多信息：** <https://yunohost.org/packaging_apps>
