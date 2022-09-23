---
aliases:
  - ihomeserver install logs media server services
tags: 
created: 2022-07-13T01:09:45-07:00
updated: 2022-07-29T02:47:18-07:00
title: ihomeserver install logs media server services
linter-yaml-title-alias: ihomeserver install logs media server services
date created: Wednesday, July 13th 2022, 1:08:25 am
date modified: Thursday, July 28th 2022, 6:32:41 pm
---

# ihomeserver install logs media server services

```cpp
kirkie@pop-os:~$ ssh root@192.168.50.26
root@192.168.50.26's password: 

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
 ─────────────────────────────────────────────────────
 DietPi v8.6.1 : 08:48 - Wed 07/13/22
 ─────────────────────────────────────────────────────
 - Device model : RPi 400 (aarch64)
 - CPU temp : 36 °C / 96 °F : Cool runnings
 - LAN IP : 192.168.50.26 (eth0)
 - MOTD : DietPi v8.6 has been released, check out all changes:
          https://dietpi.com/docs/releases/v8_6/
 ─────────────────────────────────────────────────────

 DietPi Team     : https://github.com/MichaIng/DietPi#the-dietpi-project-team
 Image by        : DietPi Core Team (pre-image: from scratch)
 Patreon Legends : Camry2731, Chris Gelatt
 Website         : https://dietpi.com/ | https://twitter.com/DietPi_
 Contribute      : https://dietpi.com/contribute.html
 Web Hosting by  : https://myvirtualserver.com

 dietpi-launcher : All the DietPi programs in one place
 dietpi-config   : Feature rich configuration tool for your device
 dietpi-software : Select optimised software for installation
 htop            : Resource monitor
 cpu             : Shows CPU information and stats

root@homeserver:~# dietpi-launcher
[ INFO ] DietPi-Software | Concurrent execution of DietPi-Software detected, retrying... (1/5)
[ INFO ] DietPi-Software | Concurrent execution of DietPi-Software detected, retrying... (2/5)
[ INFO ] DietPi-Software | Concurrent execution of DietPi-Software detected, retrying... (3/5)
[ INFO ] DietPi-Software | Concurrent execution of DietPi-Software detected, retrying... (4/5)
[ INFO ] DietPi-Software | Concurrent execution of DietPi-Software detected, retrying... (5/5)
[FAILED] DietPi-Software | Cancelled DietPi-Software due to concurrent execution

- Press any key to return to DietPi-Launcher...
root@homeserver:~# reboot
root@homeserver:~# Connection to 192.168.50.26 closed by remote host.
Connection to 192.168.50.26 closed.
kirkie@pop-os:~$ ssh root@192.168.50.26
ssh: connect to host 192.168.50.26 port 22: No route to host
kirkie@pop-os:~$ ssh root@192.168.50.26
ssh: connect to host 192.168.50.26 port 22: No route to host
kirkie@pop-os:~$ ssh root@192.168.50.26
root@192.168.50.26's password: 

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
 ─────────────────────────────────────────────────────
 DietPi v8.6.1 : 08:49 - Wed 07/13/22
 ─────────────────────────────────────────────────────
 - Device model : RPi 400 (aarch64)
 - CPU temp : 42 °C / 107 °F : Optimal temperature
 - LAN IP : 192.168.50.26 (eth0)
 - MOTD : DietPi v8.6 has been released, check out all changes:
          https://dietpi.com/docs/releases/v8_6/
 ─────────────────────────────────────────────────────

 DietPi Team     : https://github.com/MichaIng/DietPi#the-dietpi-project-team
 Image by        : DietPi Core Team (pre-image: from scratch)
 Patreon Legends : Camry2731, Chris Gelatt
 Website         : https://dietpi.com/ | https://twitter.com/DietPi_
 Contribute      : https://dietpi.com/contribute.html
 Web Hosting by  : https://myvirtualserver.com

 dietpi-launcher : All the DietPi programs in one place
 dietpi-config   : Feature rich configuration tool for your device
 dietpi-software : Select optimised software for installation
 htop            : Resource monitor
 cpu             : Shows CPU information and stats

root@homeserver:~# dietpi-launcher
[  OK  ] DietPi-Software | Initialised database
[  OK  ] DietPi-Software | Reading database
[  OK  ] DietPi-Software | DietPi-Userdata validation: /mnt/b56a2f3e-0977-43a0-8395-9036a3838a11/dietpi_userdata

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Checking for conflicts and missing inputs


 DietPi-Software
─────────────────────────────────────────────────────
 Step: Checking for prerequisite software

[ INFO ] DietPi-Software | ALSA will be reinstalled
[ INFO ] DietPi-Software | Python 3 will be reinstalled
[ INFO ] DietPi-Software | MariaDB will be reinstalled
[ INFO ] DietPi-Software | PHP will be reinstalled
[ INFO ] DietPi-Software | MPD will be installed
[ INFO ] DietPi-Software | Avahi-Daemon will be reinstalled
[ INFO ] DietPi-Software | youtube-dl will be reinstalled
[ INFO ] DietPi-Software | FFmpeg will be reinstalled
[ INFO ] DietPi-Software | PHP Composer will be reinstalled
[  OK  ] DietPi-Software | Checking network connectivity
[  OK  ] DietPi-Software | Checking DNS resolver
[  OK  ] DietPi-Software | mkdir -p /mnt/dietpi_userdata/Music /mnt/dietpi_userdata/Pictures /mnt/dietpi_userdata/Video /mnt/dietpi_userdata/downloads /var/www /opt /usr/local/bin
[  OK  ] DietPi-Software | chown dietpi:dietpi /mnt/dietpi_userdata/Music /mnt/dietpi_userdata/Pictures /mnt/dietpi_userdata/Video /mnt/dietpi_userdata/downloads
[  OK  ] DietPi-Software | chmod 0775 /mnt/dietpi_userdata/Music /mnt/dietpi_userdata/Pictures /mnt/dietpi_userdata/Video /mnt/dietpi_userdata/downloads
[ SUB1 ] DietPi-Services > unmask 
[  OK  ] DietPi-Services | unmask : avahi-daemon
[  OK  ] DietPi-Services | unmask : frpc
[  OK  ] DietPi-Services | unmask : nmbd
[  OK  ] DietPi-Services | unmask : smbd
[  OK  ] DietPi-Services | unmask : mariadb
[  OK  ] DietPi-Services | unmask : php8.1-fpm
[  OK  ] DietPi-Services | unmask : nginx
[  OK  ] DietPi-Services | unmask : icecast2
[  OK  ] DietPi-Services | unmask : darkice
[  OK  ] DietPi-Services | unmask : rtorrent
[  OK  ] DietPi-Services | unmask : nzbget
[  OK  ] DietPi-Services | unmask : logitechmediaserver
[  OK  ] DietPi-Services | unmask : raspotify
[  OK  ] DietPi-Services | unmask : tautulli
[  OK  ] DietPi-Services | unmask : plexmediaserver
[  OK  ] DietPi-Services | unmask : medusa
[  OK  ] DietPi-Services | unmask : aria2
[  OK  ] DietPi-Services | unmask : jackett
[  OK  ] DietPi-Services | unmask : sonarr
[  OK  ] DietPi-Services | unmask : radarr
[  OK  ] DietPi-Services | unmask : lidarr
[  OK  ] DietPi-Services | unmask : bazarr
[  OK  ] DietPi-Services | unmask : prowlarr
[  OK  ] DietPi-Services | unmask : motioneye
[  OK  ] DietPi-Services | unmask : grafana-server
[  OK  ] DietPi-Services | unmask : home-assistant
[  OK  ] DietPi-Services | unmask : domoticz
[  OK  ] DietPi-Services | unmask : htpc-manager
[  OK  ] DietPi-Services | unmask : docker
[  OK  ] DietPi-Services | unmask : cron
[ SUB1 ] DietPi-Services > stop 
[  OK  ] DietPi-Services | stop : cron
[  OK  ] DietPi-Services | stop : docker
[  OK  ] DietPi-Services | stop : htpc-manager
[  OK  ] DietPi-Services | stop : domoticz
[  OK  ] DietPi-Services | stop : home-assistant
[  OK  ] DietPi-Services | stop : grafana-server
[  OK  ] DietPi-Services | stop : motioneye
[  OK  ] DietPi-Services | stop : prowlarr
[  OK  ] DietPi-Services | stop : bazarr
[  OK  ] DietPi-Services | stop : lidarr
[  OK  ] DietPi-Services | stop : radarr
[  OK  ] DietPi-Services | stop : sonarr
[  OK  ] DietPi-Services | stop : jackett
[  OK  ] DietPi-Services | stop : aria2
[  OK  ] DietPi-Services | stop : medusa
[  OK  ] DietPi-Services | stop : plexmediaserver
[  OK  ] DietPi-Services | stop : tautulli
[  OK  ] DietPi-Services | stop : raspotify
[  OK  ] DietPi-Services | stop : logitechmediaserver
[  OK  ] DietPi-Services | stop : nzbget
[  OK  ] DietPi-Services | stop : rtorrent
[  OK  ] DietPi-Services | stop : darkice
[  OK  ] DietPi-Services | stop : icecast2
[  OK  ] DietPi-Services | stop : nginx
[  OK  ] DietPi-Services | stop : php8.1-fpm
[  OK  ] DietPi-Services | stop : mariadb
[  OK  ] DietPi-Services | stop : smbd
[  OK  ] DietPi-Services | stop : nmbd
[  OK  ] DietPi-Services | stop : frpc
[  OK  ] DietPi-Services | stop : avahi-daemon
[ INFO ] DietPi-Software | APT update, please wait...
Hit:1 https://download.mono-project.com/repo/debian buster InRelease
Hit:2 https://deb.debian.org/debian bookworm InRelease
Hit:3 https://download.docker.com/linux/debian bullseye InRelease
Hit:4 https://dtcooper.github.io/raspotify raspotify InRelease
Hit:5 https://downloads.plex.tv/repo/deb public InRelease
Hit:6 https://deb.debian.org/debian bookworm-updates InRelease
Hit:7 https://packages.grafana.com/oss/deb stable InRelease
Hit:8 https://download.zerotier.com/debian/bookworm bookworm InRelease
Hit:9 https://deb.debian.org/debian-security bookworm-security InRelease
Hit:10 https://deb.debian.org/debian bookworm-backports InRelease
Hit:11 https://archive.raspberrypi.org/debian bullseye InRelease
Hit:12 https://apt.sonarr.tv/debian buster InRelease
Reading package lists...
W: https://apt.sonarr.tv/debian/dists/buster/InRelease: Key is stored in legacy trusted.gpg keyring (/etc/apt/trusted.gpg), see the DEPRECATION section in apt-key(8) for details.
[  OK  ] DietPi-Software | APT update

[[ALSA]]

[[avahi-daemon]]

[[ffmpeg]]

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Python 3: Runtime system, pip package installer and development headers

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://bootstrap.pypa.io/get-pip.py
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://bootstrap.pypa.io/get-pip.py -o get-pip.py
[ INFO ] DietPi-Software | APT install for: python3-dev, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
python3-dev is already the newest version (3.10.4-1+b1).
0 upgraded, 0 newly installed, 0 to remove and 16 not upgraded.
[  OK  ] DietPi-Software | APT install for: python3-dev
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[ INFO ] DietPi-Software | python3 get-pip.py, please wait...
Collecting pip
  Using cached pip-22.1.2-py3-none-any.whl (2.1 MB)
Installing collected packages: pip
  Attempting uninstall: pip
    Found existing installation: pip 22.1.2
    Uninstalling pip-22.1.2:
      Successfully uninstalled pip-22.1.2
Successfully installed pip-22.1.2
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv
[  OK  ] DietPi-Software | python3 get-pip.py
[  OK  ] DietPi-Software | rm get-pip.py

 DietPi-Software
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
0 upgraded, 0 newly installed, 0 to remove and 16 not upgraded.
[  OK  ] DietPi-Software | APT install for: mariadb-server
[  OK  ] DietPi-Software | systemctl stop mariadb
[ INFO ] DietPi-Software | Removing obsolete SysV mysql service
[  OK  ] DietPi-Software | update-rc.d mysql remove

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
0 upgraded, 0 newly installed, 0 to remove and 16 not upgraded.
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
[  OK  ] DietPi-Software | Added setting opcache.memory_consumption=125 to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | Added setting opcache.revalidate_freq=60 to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | Added setting apc.shm_size=62M to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | Added setting apc.ttl=259200 to end of file /etc/php/8.1/mods-available/dietpi.ini
[  OK  ] DietPi-Software | phpenmod tokenizer opcache zip xmlwriter gd sqlite3 pdo sysvsem intl calendar ctype sockets xmlreader xsl dietpi exif shmop ffi readline mbstring dom pdo_sqlite mysqli iconv phar fileinfo sysvmsg pdo_mysql gettext simplexml apcu xml curl ftp sysvshm mysqlnd posix
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://raw.githubusercontent.com/amnuts/opcache-gui/master/index.php -o /var/www/opcache.php
[ INFO ] DietPi-Software | G_THREAD_START_1 | curl -sSfL https://raw.githubusercontent.com/krakjoe/apcu/master/apc.php -o /var/www/apc.php
[  OK  ] DietPi-Software | G_THREAD: All threads finished

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing PHP Composer: Package manager for PHP

[  OK  ] DietPi-Software | curl -sSfL https://getcomposer.org/composer-stable.phar -o /usr/local/bin/composer
[  OK  ] DietPi-Software | chmod +x /usr/local/bin/composer

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing MPD: music player daemon

[ INFO ] DietPi-Software | APT install for: mpd, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
The following additional packages will be installed:
  libadplug-2.3.3-0 libao-common libao4 libbinio1v5 libfaad2 libfluidsynth3
  libfmt8 libid3tag0 libinstpatch-1.0-2 libiso9660-11 libixml10 libmad0
  libmikmod3 libmodplug1 libmpcdec6 libmpdclient2 libnfs13 libpipewire-0.3-0
  libshout3 libsidplayfp6 libsmbclient libspa-0.2-modules libupnp13
  libwavpack1 libwebrtc-audio-processing1 libwildmidi2 libyajl2 libzzip-0-13
  timgm6mb-soundfont
Suggested packages:
  adplug-utils libaudio2 libsndio6.1 pipewire sidplayfp libwildmidi-config
  mpd-client pulseaudio fluid-soundfont-gm
Recommended packages:
  libpipewire-0.3-common
The following NEW packages will be installed:
  libadplug-2.3.3-0 libao-common libao4 libbinio1v5 libfaad2 libfluidsynth3
  libfmt8 libid3tag0 libinstpatch-1.0-2 libiso9660-11 libixml10 libmad0
  libmikmod3 libmodplug1 libmpcdec6 libmpdclient2 libnfs13 libpipewire-0.3-0
  libshout3 libsidplayfp6 libsmbclient libspa-0.2-modules libupnp13
  libwavpack1 libwebrtc-audio-processing1 libwildmidi2 libyajl2 libzzip-0-13
  mpd timgm6mb-soundfont
0 upgraded, 30 newly installed, 0 to remove and 16 not upgraded.
Need to get 9510 kB of archives.
After this operation, 19.7 MB of additional disk space will be used.
Get:1 https://deb.debian.org/debian bookworm/main arm64 libbinio1v5 arm64 1.5+dfsg-0.1 [24.9 kB]
Get:2 https://deb.debian.org/debian bookworm/main arm64 libadplug-2.3.3-0 arm64 2.3.3+dfsg-2 [207 kB]
Get:3 https://deb.debian.org/debian bookworm/main arm64 libao-common all 1.2.2+20180113-1.1 [11.7 kB]
Get:4 https://deb.debian.org/debian bookworm/main arm64 libao4 arm64 1.2.2+20180113-1.1 [36.3 kB]
Get:5 https://deb.debian.org/debian bookworm/main arm64 libfaad2 arm64 2.10.0-2 [156 kB]
Get:6 https://deb.debian.org/debian bookworm/main arm64 libinstpatch-1.0-2 arm64 1.1.6-1 [240 kB]
Get:7 https://deb.debian.org/debian bookworm/main arm64 timgm6mb-soundfont all 1.3-5 [5427 kB]
Get:8 https://deb.debian.org/debian bookworm/main arm64 libfluidsynth3 arm64 2.2.7-1 [227 kB]
Get:9 https://deb.debian.org/debian bookworm/main arm64 libfmt8 arm64 8.1.1+ds1-2 [101 kB]
Get:10 https://deb.debian.org/debian bookworm/main arm64 libid3tag0 arm64 0.15.1b-14 [33.3 kB]
Get:11 https://deb.debian.org/debian bookworm/main arm64 libiso9660-11 arm64 2.1.0-3 [167 kB]
Get:12 https://deb.debian.org/debian bookworm/main arm64 libixml10 arm64 1:1.8.4-2 [76.8 kB]
Get:13 https://deb.debian.org/debian bookworm/main arm64 libmad0 arm64 0.15.1b-10 [68.1 kB]
Get:14 https://deb.debian.org/debian bookworm/main arm64 libmikmod3 arm64 3.3.11.1-6 [126 kB]
Get:15 https://deb.debian.org/debian bookworm/main arm64 libmodplug1 arm64 1:0.8.9.0-3 [152 kB]
Get:16 https://deb.debian.org/debian bookworm/main arm64 libmpcdec6 arm64 2:0.1~r495-2 [31.7 kB]
Get:17 https://deb.debian.org/debian bookworm/main arm64 libmpdclient2 arm64 2.20-1 [46.1 kB]
Get:18 https://deb.debian.org/debian bookworm/main arm64 libnfs13 arm64 4.0.0-1 [96.0 kB]
Get:19 https://deb.debian.org/debian bookworm/main arm64 libwebrtc-audio-processing1 arm64 0.3-1+b1 [241 kB]
Get:20 https://deb.debian.org/debian bookworm/main arm64 libspa-0.2-modules arm64 0.3.54-2 [419 kB]
Get:21 https://deb.debian.org/debian bookworm/main arm64 libpipewire-0.3-0 arm64 0.3.54-2 [255 kB]
Get:22 https://deb.debian.org/debian bookworm/main arm64 libshout3 arm64 2.4.6-1+b1 [54.0 kB]
Get:23 https://deb.debian.org/debian bookworm/main arm64 libsidplayfp6 arm64 2.3.1-1 [104 kB]
Get:24 https://deb.debian.org/debian bookworm/main arm64 libsmbclient arm64 2:4.16.2+dfsg-1 [166 kB]
Get:25 https://deb.debian.org/debian bookworm/main arm64 libupnp13 arm64 1:1.8.4-2 [140 kB]
Get:26 https://deb.debian.org/debian bookworm/main arm64 libwavpack1 arm64 5.4.0-1 [79.0 kB]
Get:27 https://deb.debian.org/debian bookworm/main arm64 libwildmidi2 arm64 0.4.3-1 [62.5 kB]
Get:28 https://deb.debian.org/debian bookworm/main arm64 libyajl2 arm64 2.1.0-3 [22.9 kB]
Get:29 https://deb.debian.org/debian bookworm/main arm64 libzzip-0-13 arm64 0.13.72+dfsg.1-1.1 [58.3 kB]
Get:30 https://deb.debian.org/debian bookworm/main arm64 mpd arm64 0.23.6-1+b2 [681 kB]
debconf: delaying package configuration, since apt-utils is not installed
Fetched 9510 kB in 3s (2841 kB/s)
                                 Selecting previously unselected package libbinio1v5:arm64.
(Reading database ... 58353 files and directories currently installed.)
Preparing to unpack .../00-libbinio1v5_1.5+dfsg-0.1_arm64.deb ...
Unpacking libbinio1v5:arm64 (1.5+dfsg-0.1) ...
Selecting previously unselected package libadplug-2.3.3-0.
Preparing to unpack .../01-libadplug-2.3.3-0_2.3.3+dfsg-2_arm64.deb ...
Unpacking libadplug-2.3.3-0 (2.3.3+dfsg-2) ...
Selecting previously unselected package libao-common.
Preparing to unpack .../02-libao-common_1.2.2+20180113-1.1_all.deb ...
Unpacking libao-common (1.2.2+20180113-1.1) ...
Selecting previously unselected package libao4:arm64.
Preparing to unpack .../03-libao4_1.2.2+20180113-1.1_arm64.deb ...
Unpacking libao4:arm64 (1.2.2+20180113-1.1) ...
Selecting previously unselected package libfaad2:arm64.
Preparing to unpack .../04-libfaad2_2.10.0-2_arm64.deb ...
Unpacking libfaad2:arm64 (2.10.0-2) ...
Selecting previously unselected package libinstpatch-1.0-2:arm64.
Preparing to unpack .../05-libinstpatch-1.0-2_1.1.6-1_arm64.deb ...
Unpacking libinstpatch-1.0-2:arm64 (1.1.6-1) ...
Selecting previously unselected package timgm6mb-soundfont.
Preparing to unpack .../06-timgm6mb-soundfont_1.3-5_all.deb ...
Unpacking timgm6mb-soundfont (1.3-5) ...
Selecting previously unselected package libfluidsynth3:arm64.
Preparing to unpack .../07-libfluidsynth3_2.2.7-1_arm64.deb ...
Unpacking libfluidsynth3:arm64 (2.2.7-1) ...
Selecting previously unselected package libfmt8:arm64.
Preparing to unpack .../08-libfmt8_8.1.1+ds1-2_arm64.deb ...
Unpacking libfmt8:arm64 (8.1.1+ds1-2) ...
Selecting previously unselected package libid3tag0:arm64.
Preparing to unpack .../09-libid3tag0_0.15.1b-14_arm64.deb ...
Unpacking libid3tag0:arm64 (0.15.1b-14) ...
Selecting previously unselected package libiso9660-11:arm64.
Preparing to unpack .../10-libiso9660-11_2.1.0-3_arm64.deb ...
Unpacking libiso9660-11:arm64 (2.1.0-3) ...
Selecting previously unselected package libixml10:arm64.
Preparing to unpack .../11-libixml10_1%3a1.8.4-2_arm64.deb ...
Unpacking libixml10:arm64 (1:1.8.4-2) ...
Selecting previously unselected package libmad0:arm64.
Preparing to unpack .../12-libmad0_0.15.1b-10_arm64.deb ...
Unpacking libmad0:arm64 (0.15.1b-10) ...
Selecting previously unselected package libmikmod3:arm64.
Preparing to unpack .../13-libmikmod3_3.3.11.1-6_arm64.deb ...
Unpacking libmikmod3:arm64 (3.3.11.1-6) ...
Selecting previously unselected package libmodplug1:arm64.
Preparing to unpack .../14-libmodplug1_1%3a0.8.9.0-3_arm64.deb ...
Unpacking libmodplug1:arm64 (1:0.8.9.0-3) ...
Selecting previously unselected package libmpcdec6:arm64.
Preparing to unpack .../15-libmpcdec6_2%3a0.1~r495-2_arm64.deb ...
Unpacking libmpcdec6:arm64 (2:0.1~r495-2) ...
Selecting previously unselected package libmpdclient2:arm64.
Preparing to unpack .../16-libmpdclient2_2.20-1_arm64.deb ...
Unpacking libmpdclient2:arm64 (2.20-1) ...
Selecting previously unselected package libnfs13:arm64.
Preparing to unpack .../17-libnfs13_4.0.0-1_arm64.deb ...
Unpacking libnfs13:arm64 (4.0.0-1) ...
Selecting previously unselected package libwebrtc-audio-processing1:arm64.
Preparing to unpack .../18-libwebrtc-audio-processing1_0.3-1+b1_arm64.deb ...
Unpacking libwebrtc-audio-processing1:arm64 (0.3-1+b1) ...
Selecting previously unselected package libspa-0.2-modules:arm64.
Preparing to unpack .../19-libspa-0.2-modules_0.3.54-2_arm64.deb ...
Unpacking libspa-0.2-modules:arm64 (0.3.54-2) ...
Selecting previously unselected package libpipewire-0.3-0:arm64.
Preparing to unpack .../20-libpipewire-0.3-0_0.3.54-2_arm64.deb ...
Unpacking libpipewire-0.3-0:arm64 (0.3.54-2) ...
Selecting previously unselected package libshout3:arm64.
Preparing to unpack .../21-libshout3_2.4.6-1+b1_arm64.deb ...
Unpacking libshout3:arm64 (2.4.6-1+b1) ...
Selecting previously unselected package libsidplayfp6:arm64.
Preparing to unpack .../22-libsidplayfp6_2.3.1-1_arm64.deb ...
Unpacking libsidplayfp6:arm64 (2.3.1-1) ...
Selecting previously unselected package libsmbclient:arm64.
Preparing to unpack .../23-libsmbclient_2%3a4.16.2+dfsg-1_arm64.deb ...
Unpacking libsmbclient:arm64 (2:4.16.2+dfsg-1) ...
Selecting previously unselected package libupnp13:arm64.
Preparing to unpack .../24-libupnp13_1%3a1.8.4-2_arm64.deb ...
Unpacking libupnp13:arm64 (1:1.8.4-2) ...
Selecting previously unselected package libwavpack1:arm64.
Preparing to unpack .../25-libwavpack1_5.4.0-1_arm64.deb ...
Unpacking libwavpack1:arm64 (5.4.0-1) ...
Selecting previously unselected package libwildmidi2:arm64.
Preparing to unpack .../26-libwildmidi2_0.4.3-1_arm64.deb ...
Unpacking libwildmidi2:arm64 (0.4.3-1) ...
Selecting previously unselected package libyajl2:arm64.
Preparing to unpack .../27-libyajl2_2.1.0-3_arm64.deb ...
Unpacking libyajl2:arm64 (2.1.0-3) ...
Selecting previously unselected package libzzip-0-13:arm64.
Preparing to unpack .../28-libzzip-0-13_0.13.72+dfsg.1-1.1_arm64.deb ...
Unpacking libzzip-0-13:arm64 (0.13.72+dfsg.1-1.1) ...
Selecting previously unselected package mpd.
Preparing to unpack .../29-mpd_0.23.6-1+b2_arm64.deb ...
Unpacking mpd (0.23.6-1+b2) ...
Setting up libmodplug1:arm64 (1:0.8.9.0-3) ...
Setting up libbinio1v5:arm64 (1.5+dfsg-0.1) ...
Setting up libiso9660-11:arm64 (2.1.0-3) ...
Setting up libmikmod3:arm64 (3.3.11.1-6) ...
Setting up libyajl2:arm64 (2.1.0-3) ...
Setting up libwebrtc-audio-processing1:arm64 (0.3-1+b1) ...
Setting up libzzip-0-13:arm64 (0.13.72+dfsg.1-1.1) ...
Setting up libnfs13:arm64 (4.0.0-1) ...
Setting up libmpcdec6:arm64 (2:0.1~r495-2) ...
Setting up libao-common (1.2.2+20180113-1.1) ...
Setting up libsidplayfp6:arm64 (2.3.1-1) ...
Setting up libid3tag0:arm64 (0.15.1b-14) ...
Setting up libspa-0.2-modules:arm64 (0.3.54-2) ...
Setting up libixml10:arm64 (1:1.8.4-2) ...
Setting up libpipewire-0.3-0:arm64 (0.3.54-2) ...
Setting up libfaad2:arm64 (2.10.0-2) ...
Setting up libshout3:arm64 (2.4.6-1+b1) ...
Setting up libmpdclient2:arm64 (2.20-1) ...
Setting up libsmbclient:arm64 (2:4.16.2+dfsg-1) ...
Setting up libao4:arm64 (1.2.2+20180113-1.1) ...
Setting up libmad0:arm64 (0.15.1b-10) ...
Setting up libwildmidi2:arm64 (0.4.3-1) ...
Setting up libwavpack1:arm64 (5.4.0-1) ...
Setting up libfmt8:arm64 (8.1.1+ds1-2) ...
Setting up timgm6mb-soundfont (1.3-5) ...
update-alternatives: using /usr/share/sounds/sf2/TimGM6mb.sf2 to provide /usr/share/sounds/sf2/default-GM.sf2 (default-GM.sf2) in auto mode
update-alternatives: using /usr/share/sounds/sf2/TimGM6mb.sf2 to provide /usr/share/sounds/sf3/default-GM.sf3 (default-GM.sf3) in auto mode
Setting up libadplug-2.3.3-0 (2.3.3+dfsg-2) ...
Setting up libinstpatch-1.0-2:arm64 (1.1.6-1) ...
Setting up libfluidsynth3:arm64 (2.2.7-1) ...
Setting up libupnp13:arm64 (1:1.8.4-2) ...
Setting up mpd (0.23.6-1+b2) ...
Processing triggers for libc-bin (2.33-7) ...
Processing triggers for hicolor-icon-theme (0.17-2) ...
[  OK  ] DietPi-Software | APT install for: mpd
[  OK  ] DietPi-Software | systemctl stop mpd
[  OK  ] DietPi-Software | mkdir /etc/systemd/system/mpd.service.d
[ INFO ] DietPi-Software | Removing obsolete SysV mpd service
[  OK  ] DietPi-Software | rm /etc/init.d/mpd
[  OK  ] DietPi-Software | update-rc.d mpd remove
[  OK  ] DietPi-Software | rm /etc/default/mpd
[  OK  ] DietPi-Software | Setting in /etc/mpd.conf adjusted: music_directory "/mnt/dietpi_userdata/Music"
[  OK  ] DietPi-Software | Setting in /etc/mpd.conf adjusted: playlist_directory "/mnt/dietpi_userdata/Music"
[  OK  ] DietPi-Software | Setting in /etc/mpd.conf adjusted: db_file "/mnt/dietpi_userdata/.mpd_cache/db_file"
[  OK  ] DietPi-Software | sed -Ei s/^[[:blank:]]*log_file[[:blank:]]+/#log_file / /etc/mpd.conf
[  OK  ] DietPi-Software | sed -Ei s/^[[:blank:]]*pid_file[[:blank:]]+/#pid_file / /etc/mpd.conf
[  OK  ] DietPi-Software | Setting in /etc/mpd.conf adjusted: state_file "/mnt/dietpi_userdata/.mpd_cache/state"
[  OK  ] DietPi-Software | Setting in /etc/mpd.conf adjusted: sticker_file "/mnt/dietpi_userdata/.mpd_cache/sticker.sql"
[  OK  ] DietPi-Software | sed -Ei s/^[[:blank:]]*user[[:blank:]]+/#user / /etc/mpd.conf
[  OK  ] DietPi-Software | sed -Ei s/^[[:blank:]]*group[[:blank:]]+/#group / /etc/mpd.conf
[  OK  ] DietPi-Software | Comment in /etc/mpd.conf converted to setting: bind_to_address "/run/mpd/socket"
[  OK  ] DietPi-Software | Verifying user "mpd" to run MPD
[  OK  ] DietPi-Software | usermod -g audio -aG dietpi -d /mnt/dietpi_userdata/.mpd_cache -s /usr/sbin/nologin mpd
[  OK  ] DietPi-Software | rm -Rf /var/lib/mpd /var/log/mpd /mnt/dietpi_userdata/.mpd_cache
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/.mpd_cache
[  OK  ] DietPi-Software | chown -R mpd:root /mnt/dietpi_userdata/.mpd_cache /etc/mpd.conf

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing myMPD: fork of ympd with improved features

[  OK  ] DietPi-Software | Checking URL: https://download.opensuse.org/repositories/home:/jcorporation/Debian_Testing/Release.key
[  OK  ] DietPi-Software | eval curl -sSfL 'https://download.opensuse.org/repositories/home:/jcorporation/Debian_Testing/Release.key' | gpg --dearmor -o /etc/apt/trusted.gpg.d/dietpi-mympd.gpg --yes
[  OK  ] DietPi-Software | eval echo 'deb https://download.opensuse.org/repositories/home:/jcorporation/Debian_Testing/ /' > /etc/apt/sources.list.d/dietpi-mympd.list
[ INFO ] DietPi-Software | APT update, please wait...
Hit:1 https://deb.debian.org/debian bookworm InRelease
Hit:2 https://download.mono-project.com/repo/debian buster InRelease
Hit:3 https://download.docker.com/linux/debian bullseye InRelease
Hit:4 https://downloads.plex.tv/repo/deb public InRelease
Hit:5 https://dtcooper.github.io/raspotify raspotify InRelease
Hit:6 https://deb.debian.org/debian bookworm-updates InRelease
Hit:7 https://download.zerotier.com/debian/bookworm bookworm InRelease
Hit:8 https://packages.grafana.com/oss/deb stable InRelease
Hit:9 https://deb.debian.org/debian-security bookworm-security InRelease
Hit:10 https://deb.debian.org/debian bookworm-backports InRelease
Hit:11 https://archive.raspberrypi.org/debian bullseye InRelease
Hit:12 https://apt.sonarr.tv/debian buster InRelease
Get:13 https://download.opensuse.org/repositories/home:/jcorporation/Debian_Testing  InRelease [1552 B]
Get:14 https://download.opensuse.org/repositories/home:/jcorporation/Debian_Testing  Packages [1527 B]
Fetched 3079 B in 6s (539 B/s)
Reading package lists...
W: https://apt.sonarr.tv/debian/dists/buster/InRelease: Key is stored in legacy trusted.gpg keyring (/etc/apt/trusted.gpg), see the DEPRECATION section in apt-key(8) for details.
[  OK  ] DietPi-Software | APT update
[ INFO ] DietPi-Software | APT install for: mympd, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
The following additional packages will be installed:
  liblua5.3-0
The following NEW packages will be installed:
  liblua5.3-0 mympd
0 upgraded, 2 newly installed, 0 to remove and 16 not upgraded.
Need to get 660 kB of archives.
After this operation, 1585 kB of additional disk space will be used.
Get:1 https://deb.debian.org/debian bookworm/main arm64 liblua5.3-0 arm64 5.3.6-1 [113 kB]
Get:2 https://download.opensuse.org/repositories/home:/jcorporation/Debian_Testing  mympd 9.3.4-1 [547 kB]
debconf: delaying package configuration, since apt-utils is not installed
Fetched 660 kB in 5s (143 kB/s)
                               Selecting previously unselected package liblua5.3-0:arm64.
(Reading database ... 58668 files and directories currently installed.)
Preparing to unpack .../liblua5.3-0_5.3.6-1_arm64.deb ...
Unpacking liblua5.3-0:arm64 (5.3.6-1) ...
Selecting previously unselected package mympd.
Preparing to unpack .../mympd_9.3.4-1_arm64.deb ...
Unpacking mympd (9.3.4-1) ...
Setting up liblua5.3-0:arm64 (5.3.6-1) ...
Setting up mympd (9.3.4-1) ...
Checking status of mympd system user and group
myMPD insta`KoelIsCool`lled
Processing triggers for libc-bin (2.33-7) ...
[  OK  ] DietPi-Software | APT install for: mympd
[  OK  ] DietPi-Software | systemctl stop mympd
[  OK  ] DietPi-Software | usermod -g dietpi mympd
[  OK  ] DietPi-Software | mympd -c
[  OK  ] DietPi-Software | mkdir -pm 0700 /var/lib/mympd/state
[  OK  ] DietPi-Software | chmod 0600 /var/lib/mympd/state/music_directory /var/lib/mympd/state/playlist_directory
[  OK  ] DietPi-Software | chown -R mympd:root /var/lib/mympd/state

[[mopidy]]

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing youtube-dl: Download videos from YouTube and other video sites

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://yt-dl.org/downloads/latest/youtube-dl
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://yt-dl.org/downloads/latest/youtube-dl -o youtube-dl
[ INFO ] DietPi-Software | APT install for: python3, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
python3 is already the newest version (3.10.4-1+b1).
0 upgraded, 0 newly installed, 0 to remove and 16 not upgraded.
[  OK  ] DietPi-Software | APT install for: python3
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[ INFO ] DietPi-Software | Updating file: /usr/local/bin/youtube-dl
[  OK  ] DietPi-Software | mv youtube-dl /usr/local/bin/youtube-dl
[  OK  ] DietPi-Software | chmod +x /usr/local/bin/youtube-dl
[  OK  ] DietPi-Software | sed -i 1s/python$/python3/ /usr/local/bin/youtube-dl

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing O!MPD: Feature-rich, web interface audio player for MPD

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | curl -sSfL https://github.com/ArturSierzant/OMPD/archive/master.tar.gz -o master.tar.gz
[  OK  ] DietPi-Software | tar xf master.tar.gz --one-top-level=/var/www
[  OK  ] DietPi-Software | rm master.tar.gz
[  OK  ] DietPi-Software | mv /var/www/OMPD-master /var/www/ompd
[  OK  ] DietPi-Software | systemctl start mariadb
[  OK  ] DietPi-Software | chown -R www-data:www-data /var/www/ompd/tmp /var/www/ompd/stream /var/www/ompd/cache

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Koel: web interface audio streamer

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://github.com/koel/koel/releases/download/v5.1.14/koel-v5.1.14.tar.gz
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://github.com/koel/koel/releases/download/v5.1.14/koel-v5.1.14.tar.gz -o koel-v5.1.14.tar.gz
[ INFO ] DietPi-Software | APT install for: php8.1-bcmath php8.1-curl php8.1-mbstring php8.1-sqlite3 php8.1-xml, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
php8.1-curl is already the newest version (8.1.5-1+b1).
php8.1-mbstring is already the newest version (8.1.5-1+b1).
php8.1-sqlite3 is already the newest version (8.1.5-1+b1).
php8.1-xml is already the newest version (8.1.5-1+b1).
The following NEW packages will be installed:
  php8.1-bcmath
0 upgraded, 1 newly installed, 0 to remove and 16 not upgraded.
Need to get 14.2 kB of archives.
After this operation, 65.5 kB of additional disk space will be used.
Get:1 https://deb.debian.org/debian bookworm/main arm64 php8.1-bcmath arm64 8.1.5-1+b1 [14.2 kB]
debconf: delaying package configuration, since apt-utils is not installed
Fetched 14.2 kB in 1s (27.0 kB/s)
                                 Selecting previously unselected package php8.1-bcmath.
(Reading database ... 61551 files and directories currently installed.)
Preparing to unpack .../php8.1-bcmath_8.1.5-1+b1_arm64.deb ...
Unpacking php8.1-bcmath (8.1.5-1+b1) ...
Setting up php8.1-bcmath (8.1.5-1+b1) ...

Creating config file /etc/php/8.1/mods-available/bcmath.ini with new versions
Processing triggers for php8.1-fpm (8.1.5-1+b1) ...
Processing triggers for php8.1-cli (8.1.5-1+b1) ...
[  OK  ] DietPi-Software | APT install for: php8.1-bcmath php8.1-curl php8.1-mbstring php8.1-sqlite3 php8.1-xml
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[  OK  ] DietPi-Software | tar xf koel-v5.1.14.tar.gz
[  OK  ] DietPi-Software | rm koel-v5.1.14.tar.gz
[  OK  ] DietPi-Software | mv koel /mnt/dietpi_userdata/koel
[  OK  ] DietPi-Software | phpenmod bcmath ctype curl fileinfo mbstring pdo_mysql pdo_sqlite sqlite3 tokenizer xml
[  OK  ] DietPi-Software | cd /mnt/dietpi_userdata/koel
[ INFO ] DietPi-Software | composer i -n, please wait...
Do not run Composer as root/super user! See https://getcomposer.org/root for details
Installing dependencies from lock file (including require-dev)
Verifying lock file contents can be installed on current platform.
Nothing to install, update or remove
Package swiftmailer/swiftmailer is abandoned, you should avoid using it. Use symfony/mailer instead.
Generating optimized autoload files
> Illuminate\Foundation\ComposerScripts::postAutoloadDump
> @php artisan package:discover
Discovered Package: aws/aws-sdk-php-laravel
Discovered Package: facade/ignition
Discovered Package: intervention/image
Discovered Package: jackiedo/dotenv-editor
Discovered Package: laravel/sanctum
Discovered Package: laravel/scout
Discovered Package: laravel/tinker
Discovered Package: laravel/ui
Discovered Package: nesbot/carbon
Discovered Package: nunomaduro/collision
Discovered Package: teamtnt/laravel-scout-tntsearch-driver
Package manifest generated successfully.
96 packages you are using are looking for funding.
Use the `composer fund` command to find out more!
> @php artisan clear-compiled
Compiled services and packages files removed!
> @php artisan cache:clear
Failed to clear cache. Make sure you have the appropriate permissions.
> @php -r "if (!file_exists('.env')) copy('.env.example', '.env');"
[  OK  ] DietPi-Software | composer i -n
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Verifying user "koel" to run Koel
[  OK  ] DietPi-Software | useradd -rMN -g dietpi -d /mnt/dietpi_userdata/koel -s /usr/sbin/nologin koel
[  OK  ] DietPi-Software | cd /mnt/dietpi_userdata/koel
[  OK  ] DietPi-Software | chmod 0600 .env
[  OK  ] DietPi-Software | chown -R koel:dietpi .
[ INFO ] DietPi-Create_MySQL_DB | Creating MariaDB database koel for user koel
[  OK  ] DietPi-Create_MySQL_DB | systemctl start mariadb
[  OK  ] Creating MariaDB database koel for user koel | Completed
[  OK  ] DietPi-Software | Desired setting in .env was already set: DB_CONNECTION=mysql
[  OK  ] DietPi-Software | Setting in .env adjusted: DB_HOST=localhost
[  OK  ] DietPi-Software | Desired setting in .env was already set: DB_DATABASE=koel
[  OK  ] DietPi-Software | Desired setting in .env was already set: DB_USERNAME=koel
[  OK  ] DietPi-Software | Setting in .env adjusted: DB_PASSWORD=******************************
[  OK  ] DietPi-Software | Setting in .env adjusted: MEDIA_PATH=/mnt/dietpi_userdata/Music
[  OK  ] DietPi-Software | Setting in .env adjusted: FFMPEG_PATH=/usr/bin/ffmpeg
[ INFO ] DietPi-Software | sudo -u koel php8.1 artisan koel:init -n --no-assets, please wait...
Attempting to install or upgrade Koel.
Remember, you can always install/upgrade manually following the guide here:
📙  https://docs.koel.dev

Running in no-interaction mode
Generating app key
Migrating database
Creating default admin account
Seeding initial data

🎆  Success! Koel can now be run from localhost with `php artisan serve`.
Log in with email admin@koel.dev and password KoelIsCool
You can also scan for media with `php artisan koel:sync`.
Again, visit 📙 https://docs.koel.dev for the official documentation.
Feeling generous and want to support Koel's development? Check out https://github.com/users/phanan/sponsorship 🤗
Thanks for using Koel. You rock! 🤘
[  OK  ] DietPi-Software | sudo -u koel php8.1 artisan koel:init -n --no-assets
[ INFO ] DietPi-Software | sudo -u koel php8.1 artisan koel:sync, please wait...
Syncing media from /mnt/dietpi_userdata/Music


 1/1 [▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓] 100%

Completed! 1 new or updated song(s), 0 unchanged song(s), and 0 invalid file(s).
[  OK  ] DietPi-Software | sudo -u koel php8.1 artisan koel:sync
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Finalising install

[  OK  ] DietPi-Software | systemctl daemon-reload
[ SUB1 ] DietPi-Services > dietpi_controlled 
[  OK  ] DietPi-Services | dietpi_controlled : avahi-daemon
[  OK  ] DietPi-Services | dietpi_controlled : frpc
[  OK  ] DietPi-Services | dietpi_controlled : nmbd
[  OK  ] DietPi-Services | dietpi_controlled : smbd
[  OK  ] DietPi-Services | dietpi_controlled : mariadb
[  OK  ] DietPi-Services | dietpi_controlled : php8.1-fpm
[  OK  ] DietPi-Services | dietpi_controlled : nginx
[  OK  ] DietPi-Services | dietpi_controlled : mpd
[  OK  ] DietPi-Services | dietpi_controlled : icecast2
[  OK  ] DietPi-Services | dietpi_controlled : darkice
[  OK  ] DietPi-Services | dietpi_controlled : rtorrent
[  OK  ] DietPi-Services | dietpi_controlled : nzbget
[  OK  ] DietPi-Services | dietpi_controlled : mympd
[  OK  ] DietPi-Services | dietpi_controlled : logitechmediaserver
[  OK  ] DietPi-Services | dietpi_controlled : mopidy
[  OK  ] DietPi-Services | dietpi_controlled : koel
[  OK  ] DietPi-Services | dietpi_controlled : raspotify
[  OK  ] DietPi-Services | dietpi_controlled : tautulli
[  OK  ] DietPi-Services | dietpi_controlled : plexmediaserver
[  OK  ] DietPi-Services | dietpi_controlled : medusa
[  OK  ] DietPi-Services | dietpi_controlled : aria2
[  OK  ] DietPi-Services | dietpi_controlled : jackett
[  OK  ] DietPi-Services | dietpi_controlled : sonarr
[  OK  ] DietPi-Services | dietpi_controlled : radarr
[  OK  ] DietPi-Services | dietpi_controlled : lidarr
[  OK  ] DietPi-Services | dietpi_controlled : bazarr
[  OK  ] DietPi-Services | dietpi_controlled : prowlarr
[  OK  ] DietPi-Services | dietpi_controlled : motioneye
[  OK  ] DietPi-Services | dietpi_controlled : grafana-server
[  OK  ] DietPi-Services | dietpi_controlled : home-assistant
[  OK  ] DietPi-Services | dietpi_controlled : domoticz
[  OK  ] DietPi-Services | dietpi_controlled : htpc-manager
[  OK  ] DietPi-Services | dietpi_controlled : docker
[  OK  ] DietPi-Services | dietpi_controlled : cron

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Install completed

[  OK  ] DietPi-Survey | Sending survey data
[ SUB1 ] DietPi-Services > restart 
[  OK  ] DietPi-Services | restart : avahi-daemon
[  OK  ] DietPi-Services | restart : frpc
[  OK  ] DietPi-Services | restart : nmbd
[  OK  ] DietPi-Services | restart : smbd
[  OK  ] DietPi-Services | restart : mariadb
[  OK  ] DietPi-Services | restart : php8.1-fpm
[  OK  ] DietPi-Services | restart : nginx
[  OK  ] DietPi-Services | restart : mpd
[  OK  ] DietPi-Services | restart : icecast2
[  OK  ] DietPi-Services | restart : darkice
[  OK  ] DietPi-Services | restart : rtorrent
[  OK  ] DietPi-Services | restart : nzbget
[  OK  ] DietPi-Services | restart : mympd
[  OK  ] DietPi-Services | restart : logitechmediaserver
[  OK  ] DietPi-Services | restart : mopidy
[  OK  ] DietPi-Services | restart : koel
[  OK  ] DietPi-Services | restart : raspotify
[  OK  ] DietPi-Services | restart : tautulli
[  OK  ] DietPi-Services | restart : plexmediaserver
[  OK  ] DietPi-Services | restart : medusa
[  OK  ] DietPi-Services | restart : aria2
[  OK  ] DietPi-Services | restart : jackett
[  OK  ] DietPi-Services | restart : sonarr
[  OK  ] DietPi-Services | restart : radarr
[  OK  ] DietPi-Services | restart : lidarr
[  OK  ] DietPi-Services | restart : bazarr
[  OK  ] DietPi-Services | restart : prowlarr
[  OK  ] DietPi-Services | restart : motioneye
[  OK  ] DietPi-Services | restart : grafana-server
[  OK  ] DietPi-Services | restart : home-assistant
[  OK  ] DietPi-Services | restart : dom[  OK  ] DietPi-Services | restart : htpc-manager
[  OK  ] DietPi-Services | restart : docker
[  OK  ] DietPi-Services | restart : cron
```
