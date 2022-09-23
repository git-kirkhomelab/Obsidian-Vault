---
aliases:
  - php
tags: 
created: 2022-07-12T21:14:34-07:00
updated: 2022-07-29T02:47:12-07:00
title: php
linter-yaml-title-alias: php
date created: Tuesday, July 12th 2022, 9:13:33 pm
date modified: Thursday, July 28th 2022, 6:32:39 pm
---

# php

```ad-abstract
Hypertext preprocessor for dynamic web content 
```

## Install logs

```cpp 
 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing PHP: Hypertext Preprocessor for dynamic web content

[ INFO ] DietPi-Software | APT install for: php8.1-fpm php8.1-apcu php8.1-curl php8.1-gd php8.1-mbstring php8.1-xml php8.1-zip php8.1-mysql php8.1-sqlite3, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
php8.1-apcu is already the newest version (5.1.21+4.0.11-7).
php8.1-curl is already the newest version (8.1.5-1+b1).
php8.1-fpm is already the newest version (8.1.5-1+b1).
php8.1-gd is already the newest version (8.1.5-1+b1).
php8.1-mbstring is already the newest version (8.1.5-1+b1).
php8.1-mysql is already the newest version (8.1.5-1+b1).
php8.1-sqlite3 is already the newest version (8.1.5-1+b1).
php8.1-xml is already the newest version (8.1.5-1+b1).
php8.1-zip is already the newest version (8.1.5-1+b1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: php8.1-fpm php8.1-apcu php8.1-curl php8.1-gd php8.1-mbstring php8.1-xml php8.1-zip php8.1-mysql php8.1-sqlite3
[ INFO ] DietPi-Software | APT purge for: libapache2-mod-php*, please wait...
[ INFO ] DietPi-Software | None of the requested packages are currently installed. Aborting...
[  OK  ] DietPi-Software | APT purge for: libapache2-mod-php*
[  OK  ] DietPi-Software | rm -Rf /etc/php/*/apache2 /var/lib/php/modules/*/apache2
[  OK  ] DietPi-Software | Desired setting in /etc/php/8.1/fpm/pool.d/www.conf was already set: pm.max_children = 12
[  OK  ] DietPi-Software | Desired setting in /etc/php/8.1/fpm/pool.d/www.conf was already set: pm.start_servers = 4
[  OK  ] DietPi-Software | Desired setting in /etc/php/8.1/fpm/pool.d/www.conf was already set: pm.min_spare_servers = 4
[  OK  ] DietPi-Software | Desired setting in /etc/php/8.1/fpm/pool.d/www.conf was already set: pm.max_spare_servers = 4
[  OK  ] DietPi-Software | Desired setting in /etc/php/8.1/fpm/pool.d/www.conf was already set: env[PATH] = /usr/local/bin:/usr/bin:/bin
[  OK  ] DietPi-Software | mkdir -p /run/php_sessions
[  OK  ] DietPi-Software | chmod 1733 /run/php_sessions
[  OK  ] DietPi-Software | Added setting session.save_path="/run/php_sessions" to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | Added setting upload_tmp_dir="/tmp" to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | Added setting upload_max_filesize=512M to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | Added setting post_max_size=512M to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | Added setting opcache.memory_consumption=128 to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | Added setting opcache.revalidate_freq=60 to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | Added setting apc.shm_size=64M to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | Added setting apc.ttl=259200 to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | phpenmod tokenizer opcache zip xmlwriter gd sqlite3 pdo sysvsem calendar ctype sockets xmlreader xsl dietpi exif shmop ffi readline mbstring dom pdo_sqlite mysqli iconv phar fileinfo sysvmsg pdo_mysql gettext simplexml apcu xml curl ftp sysvshm mysqlnd posix
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://raw.githubusercontent.com/amnuts/opcache-gui/master/index.php -o /var/www/opcache.php
[ INFO ] DietPi-Software | G_THREAD_START_1 | curl -sSfL https://raw.githubusercontent.com/krakjoe/apcu/master/apc.php -o /var/www/apc.php
[  OK  ] DietPi-Software | G_THREAD: All threads finished
