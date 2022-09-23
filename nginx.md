---
aliases:
  - nginx
tags: 
created: 2022-07-12T21:06:49-07:00
updated: 2022-07-29T02:47:07-07:00
title: nginx
linter-yaml-title-alias: nginx
date created: Tuesday, July 12th 2022, 9:04:04 pm
date modified: Thursday, July 28th 2022, 6:32:55 pm
---

# nginx

```ad-abstract
Lightweight webserver 
```

## Install logs

```cpp
# DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[Nginx]]: Lightweight webserver 

[ INFO ] DietPi-Software | APT install for: nginx-light, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
nginx-light is already the newest version (1.20.2-2+b2).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: nginx-light
[  OK  ] DietPi-Software | systemctl stop nginx
[  OK  ] DietPi-Software | /etc/nginx/nginx.conf: backup to /etc/nginx/nginx.conf.bak_120722_2
[ INFO ] DietPi-Software | For a full list of backup items, please see /var/tmp/dietpi/logs/G_BACKUP_FP.db
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | curl -sSfL https://raw.githubusercontent.com/MichaIng/DietPi/master/.conf/dps_85/nginx.conf -o nginx.conf
[ INFO ] DietPi-Software | Updating file: /etc/nginx/nginx.conf
[  OK  ] DietPi-Software | mv nginx.conf /etc/nginx/nginx.conf
[  OK  ] DietPi-Software | sed -i s#/run/php/php.*-fpm.sock#/run/php/php8.1-fpm.sock#g /etc/nginx/nginx.conf
[  OK  ] DietPi-Software | sed -i /worker_processes/c\worker_processes 4; /etc/nginx/nginx.conf
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | curl -sSfL https://raw.githubusercontent.com/MichaIng/DietPi/master/.conf/dps_85/nginx.default -o nginx.default
[ INFO ] DietPi-Software | Updating file: /etc/nginx/sites-available/default
[  OK  ] DietPi-Software | mv nginx.default /etc/nginx/sites-available/default
```
---

Link to original note: [[Complete initial install logs]]
