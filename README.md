# Lufi for YunoHost

## Lufi c'est quoi ?

Il stocke et vous permet de les télécharger.

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