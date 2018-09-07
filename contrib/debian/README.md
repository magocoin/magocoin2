
Debian
====================
This directory contains files used to package epsd/eps-qt
for Debian-based Linux systems. If you compile epsd/eps-qt yourself, there are some useful files here.

## eps: URI support ##


eps-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install eps-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your epsqt binary to `/usr/bin`
and the `../../share/pixmaps/eps128.png` to `/usr/share/pixmaps`

eps-qt.protocol (KDE)

