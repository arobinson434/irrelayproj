# IrRelay Project
This repo houses my external buildroot project for an Ir Relay. It contains all
of the needed configs and external packages needed for the project. It is
intended to run on a Raspberry Pi Zero 2 W.

## Building
To configure buildroot to use this repo, simply run the following in the root of
your buildroot tree:
```
make BR2_EXTERNAL=<path_to_this_project> rpiz2w_irrelay_defconfig
```

After that, you should be good to go!

Note, you may want to add a `PSK` file in `board/rootfs_overlay/var/lib/iwd/` so
that the board will auto connect to your WiFi.
