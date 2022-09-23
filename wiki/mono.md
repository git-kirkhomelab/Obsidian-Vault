---
aliases:
  - mono
tags: 
created: 2022-07-12T08:25:47-07:00
updated: 2022-07-29T02:47:04-07:00
title: mono
date created: Tuesday, July 12th 2022, 8:24:29 am
date modified: Thursday, July 28th 2022, 6:32:34 pm
linter-yaml-title-alias: mono
---

# mono

```ad-abstract
Runtime libraries and repository 
```

# Install logs

```c
 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[Mono]]: Runtime libraries and repository

[  OK  ] DietPi-Software | curl -sSfL https://download.mono-project.com/repo/xamarin_ring.gpg -o /etc/apt/trusted.gpg.d/dietpi-mono.gpg
[  OK  ] DietPi-Software | eval echo 'deb https://download.mono-project.com/repo/debian/ buster main' > /etc/apt/sources.list.d/dietpi-mono.list
[ INFO ] DietPi-Software | APT update, please wait...
Hit:1 https://download.mono-project.com/repo/debian buster InRelease
Hit:2 https://downloads.plex.tv/repo/deb public InRelease
Hit:3 https://deb.debian.org/debian bookworm InRelease
Hit:4 https://packages.grafana.com/oss/deb stable InRelease
Hit:5 https://download.zerotier.com/debian/bookworm bookworm InRelease
Hit:6 https://deb.debian.org/debian bookworm-updates InRelease
Hit:7 https://deb.debian.org/debian-security bookworm-security InRelease
Hit:8 https://archive.raspberrypi.org/debian bullseye InRelease
Hit:9 https://deb.debian.org/debian bookworm-backports InRelease
Reading package lists...
[  OK  ] DietPi-Software | APT update
[ INFO ] DietPi-Software | APT install for: mono-devel, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
mono-devel is already the newest version (6.12.0.182-0xamarin1+debian10b1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: mono-devel
[  OK  ] DietPi-Software | rm -f /tmp/mono*
```
