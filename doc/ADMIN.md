# App configuration

Modify the file `__INSTALL_DIR__/lufi.conf` with the command line interface:

```
yunohost app shell __APP__
nano lufi.conf
```

Then `CTRL+O` and `CTRL+X` to save and quit.

# In case of major YunoHost version upgrade

Try to perform a forced app upgrade, because one of its binaries, `carton`, needs to redeployed with the new system libraries.