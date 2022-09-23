---
aliases:
  - X.org X Server
tags: 
created: 2022-07-12T05:36:22-07:00
updated: 2022-07-29T02:47:09-07:00
title: X.org X Server
linter-yaml-title-alias: X.org X Server
date created: Tuesday, July 12th 2022, 5:34:50 am
date modified: Thursday, July 28th 2022, 6:32:31 pm
---

# X.org X Server

```ad-abstract
aka X11 - X Window System implementation

```

## Install logs

```bash
DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing X.Org X Server: aka X11 - X Window System implementation

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://raw.githubusercontent.com/MichaIng/DietPi/master/.conf/dps_6/98-dietpi-disable_dpms.conf
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://raw.githubusercontent.com/MichaIng/DietPi/master/.conf/dps_6/98-dietpi-disable_dpms.conf -o 98-dietpi-disable_dpms.conf
[ INFO ] DietPi-Software | APT install for: xserver-xorg-core xserver-xorg-input-libinput xinit dbus-x11 xfonts-base x11-xserver-utils x11-utils mesa-utils mesa-utils-extra xserver-xorg-video-fbdev, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
dbus-x11 is already the newest version (1.14.0-1).
mesa-utils is already the newest version (8.5.0-1).
x11-utils is already the newest version (7.7+5).
x11-xserver-utils is already the newest version (7.7+9).
xfonts-base is already the newest version (1:1.0.5).
xinit is already the newest version (1.4.0-1).
xserver-xorg-core is already the newest version (2:21.1.3-2+b1).
xserver-xorg-input-libinput is already the newest version (1.2.1-1+b1).
xserver-xorg-video-fbdev is already the newest version (1:0.5.0-2).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: xserver-xorg-core xserver-xorg-input-libinput xinit dbus-x11 xfonts-base x11-xserver-utils x11-utils mesa-utils mesa-utils-extra xserver-xorg-video-fbdev
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[ INFO ] DietPi-Software | Updating file: /etc/X11/xorg.conf.d/98-dietpi-disable_dpms.conf
[  OK  ] DietPi-Software | mv 98-dietpi-disable_dpms.conf /etc/X11/xorg.conf.d/98-dietpi-disable_dpms.conf

```
