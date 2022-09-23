---
aliases:
  - samba server
tags: 
created: 2022-07-12T08:33:46-07:00
updated: 2022-07-29T02:50:37-07:00
title: samba server
linter-yaml-title-alias: samba server
date created: Tuesday, July 12th 2022, 8:32:03 am
date modified: Thursday, July 28th 2022, 6:32:32 pm
---

# samba server

```ad-abstract
Feature-rich SMB/CIFS server 
```

```c
 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Samba Server: Feature-rich SMB/CIFS server

[  OK  ] DietPi-Software | rm -Rf /var/cache/samba
[  OK  ] DietPi-Software | ln -s /run/samba-cache /var/cache/samba
[ INFO ] DietPi-Software | APT install for: samba, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
samba is already the newest version (2:4.16.2+dfsg-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: samba
[  OK  ] DietPi-Software | systemctl stop nmbd smbd
```
