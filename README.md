## Talk Calendar (libflite)

This version of Talk Calendar uses the [Flite API](http://cmuflite.org/doc/flite_7.html#C-example). This provides an elegant programming solution to integrating speech synthesis into an application.  Unfortunately, as I discovered, a number of distros do not have the Flite shared library in their repositories. Use [packages.org](https://pkgs.org/) to check if your distro supports libFlite. Because of this issue the main [Talk Calendar](https://github.com/crispinprojects/talkcalendar) project uses a compiled [Flite](http://www.festvox.org/flite/) binary which must be located in the working directory of the Talk Calendar executable making it universal across different distributions.

This repository which contains a libFlite version of Talk Calendar.

### Building on Ubuntu 24.04 x86 Hardware

To build Talk Calendar from source you need the gcc compiler, GTK4, GLIB, SQLITE and Flite development libraries. You need to install the following packages.

```
sudo apt install build-essential
sudo apt install libgtk-4-dev
sudo apt install libasound2-dev
sudo apt install sqlite3
sudo apt install libsqlite3-dev
sudo apt install flite1-dev
```

The packages:

```
sudo apt install libglib2.0-dev
sudo apt install alsa-utils
```

are needed but should be installed by default. 

To check the installed Sqlite 3 version use the command below.

```
sqlite3 --version
```

To determine which version of GTK4 is running on a Debian/Ubuntu system use the following terminal command.

```
dpkg -l | grep libgtk*
```

Use the MAKEFILE to compile Talk Calendar. Just run "make" inside the source code folder.

```
make
```

To run Talk Calendar from the terminal use

```
./talkcalendar
```

## License

GTK is released under the terms of the [GNU Lesser General Public License version 2.1](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html). Consequently, Talk Calendar is licensed under the same LGPL v2.1 license.

The Flite (Festival Lite) speech synthesizer has a BSD-like [license](https://github.com/festvox/flite/blob/master/COPYING).

## Acknowledgements

* [GTK](https://www.gtk.org/)

* GTK is a free and open-source project maintained by GNOME and an active community of contributors. GTK is released under the terms of the [GNU Lesser General Public License version 2.1](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html).

* [GTK4 API](https://docs.gtk.org/gtk4/index.html)

* [GObject API](https://docs.gtk.org/gobject/index.html)

* [Glib API](https://docs.gtk.org/glib/index.html)

* [Gio API](https://docs.gtk.org/gio/index.html)

* [Geany](https://www.geany.org/) is a lightweight source-code editor (version 2 now uses GTK3). [GPL v2 license](https://www.gnu.org/licenses/old-licenses/gpl-2.0.txt)

* [Sqlite](https://www.sqlite.org/index.html) is open source and in the [public domain](https://www.sqlite.org/copyright.html).

* [Flite](http://www.festvox.org/flite/) Flite (festival-lite) is a small fast portable speech synthesis system. The core Flite library was originally developed by Alan W Black and the history of the project together with other contributors can be found [here](https://github.com/festvox/flite). Flite is free software and has a BSD-like [license](https://github.com/festvox/flite/blob/master/COPYING). The BSD license is compatible with most other [open source licenses](https://www.gnu.org/licenses/gpl-faq.en.html#AllCompatibility). Flite is an official Debian package and labelled [DFGS free](https://blends.debian.org/accessibility/tasks/speechsynthesis).

* Flite [API](http://cmuflite.org/doc/flite_7.html#C-example)





