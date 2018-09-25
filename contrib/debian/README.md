
Debian
====================
This directory contains files used to package magocoind/magocoin-qt
for Debian-based Linux systems. If you compile magocoind/magocoin-qt yourself, there are some useful files here.

## magocoin: URI support ##


magocoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install magocoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your magocoinqt binary to `/usr/bin`
and the `../../share/pixmaps/magocoin128.png` to `/usr/share/pixmaps`

magocoin-qt.protocol (KDE)

