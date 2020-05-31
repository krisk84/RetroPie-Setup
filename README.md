RetroPie-Setup for ASUS TinkerBoard, ODROID C2, ODROID XU4, Nvidia Jetson Platforms, and more
==============
RetroPie-Setup modified for use on ASUS TinkerBoard, ODROID C2, and ODROID XU4 boards. I had these boards sitting around and having found some spare time during the COVID-19 quarantine I wanted to make the best use of them (and my time). Sure there is already support for gaming emulation on these boards from projects such as Lakka, Recalbox, and others but I prefer RetroPie and the full use of the underlying distribution.

Developed on:

ASUS TinkerBoard Armbian Ubuntu 18.04

ODROID XU4 ODROID Ubuntu 18.04

ODROID C2 Armbian Debian bullseye

Hardware Notes
-------------

- GLES on the TinkerBoard is accomplished using ARM Mali binaries from RockChip with updates for Ubuntu style GLES, EGL, and Mesa deb package formatting. This is pretty brittle and likely to break on different distributions due to the complexity of distribution provided packages/libraries and the formatting of the RockChip provided debs. It's a mess.

- GLES on the Odroid XU4 "just works" with mali-fbdev from the ODROID Ubuntu 18.04 image.

- GLES on the ODROID C2 works via the Armbian 5.5 kernel lima driver and the updated MESA support from Debian bullseye.

General Usage
-------------

Shell script to setup the Raspberry Pi, Vero4K, ODroid-C1/C2/XU4 or a PC running Ubuntu with many emulators and games, using EmulationStation as the graphical front end. Bootable pre-made images for the Raspberry Pi are available for those that want a ready to go system, downloadable from the releases section of GitHub or via our website at https://retropie.org.uk

This script is designed for use on Raspbian on the Raspberry Pi, OSMC on the Vero4K or Ubuntu on the ODroid-C1 or a PC.

To run the RetroPie Setup Script make sure that your APT repositories are up-to-date and that Git is installed:

```shell
sudo apt-get update
sudo apt-get dist-upgrade
sudo apt-get install git
```

Then you can download the latest RetroPie setup script with

```shell
cd
git clone --depth=1 https://github.com/RetroPie/RetroPie-Setup.git
```

The script is executed with 

```shell
cd RetroPie-Setup
sudo ./retropie_setup.sh
```

When you first run the script it may install some additional packages that are needed.

Binaries and Sources
--------------------

On the Raspberry Pi, RetroPie Setup offers the possibility to install from binaries or source. For other supported platforms only a source install is available. Installing from binary is recommended on a Raspberry Pi as building everything from source can take a long time.

For more information visit the blog at https://retropie.org.uk or the repository at https://github.com/RetroPie/RetroPie-Setup.

Wiki
----

You can find useful information about several components or for several frequently asked questions in the [wiki](https://github.com/RetroPie/RetroPie-Setup/wiki) of the RetroPie Script. If you think that there is something missing, you are invited to add it to the wiki.


Thanks
------

This script just simplifies the usage of the great works of many other people that enjoy the spirit of retrogaming. Many thanks go to them!
