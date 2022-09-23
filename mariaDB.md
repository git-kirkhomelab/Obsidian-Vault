---
aliases:
  - mariaDB
tags: 
created: 2022-07-12T21:10:47-07:00
updated: 2022-07-29T02:46:58-07:00
title: mariaDB
linter-yaml-title-alias: mariaDB
date created: Tuesday, July 12th 2022, 9:09:00 pm
date modified: Thursday, July 28th 2022, 6:32:56 pm
---

# mariaDB

```ad-abstract
Persistent cached file-per-table database server 
```

## Install logs

```cpp
# DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing MariaDB: Persistent cached file-per-table database server

[ INFO ] DietPi-Software | Preparing database directory at: /mnt/dietpi_userdata/mysql
[ INFO ] DietPi-Software | /mnt/dietpi_userdata/mysql exists, will migrate containing databases
[  OK  ] DietPi-Software | rm -Rf /var/lib/mysql
[  OK  ] DietPi-Software | ln -s /mnt/dietpi_userdata/mysql /var/lib/mysql
[ INFO ] DietPi-Software | APT install for: mariadb-server, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
mariadb-server is already the newest version (1:10.6.8-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: mariadb-server
[  OK  ] DietPi-Software | systemctl stop mariadb
[ INFO ] DietPi-Software | Removing obsolete SysV mysql service
[  OK  ] DietPi-Software | update-rc.d mysql remove
```
---

Link to original note: [[Complete initial install logs]]
