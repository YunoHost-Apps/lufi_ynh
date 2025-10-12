# Configuration de l'app

Modifiez le fichier brut `__INSTALL_DIR__/lufi.conf` via la ligne de commande:

```
yunohost app shell __APP__
nano lufi.conf
```

Puis `CTRL+O` et `CTRL+X` pour enregistrer et quitter.

# En cas de changement de version majeure de YunoHost

Tentez une mise à jour forcée de l'application, car l'un de ses exécutables, `carton`, a besoin d'être redéployé avec les nouvelles bibliothèques du système.