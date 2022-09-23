---
aliases:
  - Complete initial install logs
tags: 
created: 2022-07-13T09:06:37-07:00
updated: 2022-07-29T02:47:19-07:00
title: Complete initial install logs
linter-yaml-title-alias: Complete initial install logs
date created: Tuesday, July 12th 2022, 6:24:32 am
date modified: Thursday, July 28th 2022, 6:32:44 pm
---
f---
aliases: homeserver install logs
tags: #logs #install #software
created: 2022-07-12T06:25:24-07:00
updated: 2022-07-13T04:52:43-07:00
title: Complete initial install logs
date created: Tuesday, July 12th 2022, 6:24:32 am
date modified: Tuesday, July 12th 2022, 6:35:07 pm
---

# Complete initial install logs

```c
DietPi-Software
─────────────────────────────────────────────────────
 Step: Checking for prerequisite software

[ INFO ] DietPi-Software | PHP will be installed
[ INFO ] DietPi-Software | MariaDB will be installed
[ INFO ] DietPi-Software | Nginx will be installed
[ INFO ] DietPi-Software | SQLite will be installed
[ INFO ] DietPi-Software | UnRAR will be installed
[ INFO ] DietPi-Software | ALSA will be installed
[ INFO ] DietPi-Software | X.Org X Server will be installed
[ INFO ] DietPi-Software | FFmpeg will be installed
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
[  OK  ] DietPi-Services | unmask : rtorrent
[  OK  ] DietPi-Services | unmask : plexmediaserver
[  OK  ] DietPi-Services | unmask : medusa
[  OK  ] DietPi-Services | unmask : aria2
[  OK  ] DietPi-Services | unmask : motioneye
[  OK  ] DietPi-Services | unmask : grafana-server
[  OK  ] DietPi-Services | unmask : cron
[ SUB1 ] DietPi-Services > stop 
[  OK  ] DietPi-Services | stop : cron
[  OK  ] DietPi-Services | stop : grafana-server
[  OK  ] DietPi-Services | stop : motioneye
[  OK  ] DietPi-Services | stop : aria2
[  OK  ] DietPi-Services | stop : medusa
[  OK  ] DietPi-Services | stop : plexmediaserver
[  OK  ] DietPi-Services | stop : rtorrent
[  OK  ] DietPi-Services | stop : nginx
[  OK  ] DietPi-Services | stop : php8.1-fpm
[  OK  ] DietPi-Services | stop : mariadb
[  OK  ] DietPi-Services | stop : smbd
[  OK  ] DietPi-Services | stop : nmbd
[  OK  ] DietPi-Services | stop : frpc
[  OK  ] DietPi-Services | stop : avahi-daemon
[ INFO ] DietPi-Software | APT update, please wait...
Hit:1 https://downloads.plex.tv/repo/deb public InRelease
Hit:2 https://download.mono-project.com/repo/debian buster InRelease
Hit:3 https://packages.grafana.com/oss/deb stable InRelease
Hit:4 https://deb.debian.org/debian bookworm InRelease
Hit:5 https://deb.debian.org/debian bookworm-updates InRelease
Hit:6 https://download.zerotier.com/debian/bookworm bookworm InRelease
Hit:7 https://archive.raspberrypi.org/debian bullseye InRelease
Hit:8 https://deb.debian.org/debian-security bookworm-security InRelease
Hit:9 https://deb.debian.org/debian bookworm-backports InRelease
Reading package lists...
[  OK  ] DietPi-Software | APT update

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[ALSA]]: Advanced Linux Sound Architecture

[ SUB1 ] DietPi-Set_hardware > soundcard (rpi-bcm2835-auto)
[ INFO ] DietPi-Set_hardware | Checking for required APT packages: alsa-utils
[ INFO ] DietPi-Set_hardware | Resetting all sound card settings...
[  OK  ] DietPi-Set_hardware | rm /etc/asound.conf
[  OK  ] DietPi-Set_hardware | rm /var/lib/alsa/asound.state
[  OK  ] DietPi-Set_hardware | sed -Ei s/^[[:blank:]]*(hdmi_drive(:[01])?=.*$)/#\1/ /boot/config.txt
[  OK  ] DietPi-Set_hardware | sed -Ei /^[[:blank:]]*dtoverlay=dietpi-disable_(hdmi_audio|headphones)/d /boot/config.txt
[  OK  ] DietPi-Set_hardware | Setting in /boot/config.txt adjusted: dtparam=audio=off
[  OK  ] DietPi-Set_hardware | sed -Ei /^[[:blank:]]*dtoverlay=vc4-kms-v3d(-pi4)?(,|$)/s/$/,noaudio/ /boot/config.txt
[ INFO ] DietPi-Set_hardware | Applying new sound card settings...
[  OK  ] DietPi-Set_hardware | Desired setting in /boot/dietpi.txt was already set: CONFIG_SOUNDCARD=rpi-bcm2835-auto
[  OK  ] DietPi-Set_hardware | Setting in /boot/config.txt adjusted: dtparam=audio=on
[  OK  ] DietPi-Set_hardware | sed -Ei /^[[:blank:]]*dtoverlay=vc4-kms-v3d(-pi4)?,/s/,noaudio(,|$)/\1/ /boot/config.txt
[  OK  ] DietPi-Set_hardware | alsactl -g store
[  OK  ] soundcard rpi-bcm2835-auto | Completed

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[x.org x server|X.org X Server]]X.Org X Server: aka X11 - X Window System implementation

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

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[avahi-daemon]]avahi-Daemon: hostname broadcast (mac, pc bonjour)

[ INFO ] DietPi-Software | APT install for: avahi-daemon, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
avahi-daemon is already the newest version (0.8-6).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: avahi-daemon
[  OK  ] DietPi-Software | systemctl stop avahi-daemon

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[build-essentials]]build-Essential: GNU C/C++ compiler, development libraries and headers

[ INFO ] DietPi-Software | APT install for: g++ make automake, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
automake is already the newest version (1:1.16.5-1.3).
g++ is already the newest version (4:11.2.0-2).
make is already the newest version (4.3-4.1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: g++ make automake

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[git]]Git: Clone and manage Git repositories locally

[ INFO ] DietPi-Software | APT install for: git, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
git is already the newest version (1:2.35.1-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: git

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[logrotate]]Logrotate: Rotates and compresses old log files in /var/log

[ INFO ] DietPi-Software | APT install for: logrotate, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
logrotate is already the newest version (3.20.1-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: logrotate

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[beets]]Beets: music organizer and manager

[  OK  ] DietPi-Software | chown -R dietpi:audio /mnt/dietpi_userdata/beets
[  OK  ] DietPi-Software | chmod -R g+w /mnt/dietpi_userdata/beets
[ INFO ] DietPi-Software | APT install for: beets, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
beets is already the newest version (1.6.0-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: beets

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[rsyslog]]Rsyslog: Writes system logs (journalctl) as plain text files to /var/log

[  OK  ] DietPi-Software | systemctl stop rsyslog
[ INFO ] DietPi-Software | APT install for: rsyslog, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
rsyslog is already the newest version (8.2206.0-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: rsyslog
[  OK  ] DietPi-Software | systemctl enable --now rsyslog

 DietPi-Software ^xt--v
─────────────────────────────────────────────────────
 Step: Installing [[ffmpeg]]FFmpeg: Audio & video codec libary and programs

[ SUB1 ] DietPi-Set_hardware > rpi-codec (enable)
[  OK  ] DietPi-Set_hardware | Desired setting in /boot/config.txt was already set: dtoverlay=rpivid-v4l2
[  OK  ] rpi-codec enable | Completed
[ INFO ] DietPi-Software | APT install for: ffmpeg, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
ffmpeg is already the newest version (7:5.0.1-3).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: ffmpeg


 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[Node.js]]: JavaScript runtime environment

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://raw.githubusercontent.com/MichaIng/nodejs-linux-installer/master/node-install.sh
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://raw.githubusercontent.com/MichaIng/nodejs-linux-installer/master/node-install.sh -o node-install.sh
[ INFO ] DietPi-Software | APT install for: libatomic1, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
libatomic1 is already the newest version (12.1.0-2).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: libatomic1
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[  OK  ] DietPi-Software | chmod +x node-install.sh
[ INFO ] DietPi-Software | ./node-install.sh, please wait...
Universal Node.js Linux Installer by github.com/taaem, updated by github.com/MichaIng
root permissions verified
Searching latest stable version for aarch64 ...
Found latest stable version for aarch64: node-v18.5.0-linux-arm64.tar.gz
Downloading https://nodejs.org/dist/latest/node-v18.5.0-linux-arm64.tar.gz ...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 42.2M  100 42.2M    0     0  2240k      0  0:00:19  0:00:19 --:--:-- 1641k
Finished downloading!
Installing /tmp/node.tar.gz ...
removed '/tmp/node.tar.gz'
Finished installing!
[  OK  ] DietPi-Software | ./node-install.sh
[  OK  ] DietPi-Software | rm node-install.sh

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[Python 3]]: Runtime system, pip package installer and development headers

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://bootstrap.pypa.io/get-pip.py
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://bootstrap.pypa.io/get-pip.py -o get-pip.py
[ INFO ] DietPi-Software | APT install for: python3-dev, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
python3-dev is already the newest version (3.10.4-1+b1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
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

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[Go]]: Runtime environment and package installer

[  OK  ] DietPi-Software | rm -R /usr/local/go
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | curl -sSfL https://golang.org/dl/go1.18.3.linux-arm64.tar.gz -o go1.18.3.linux-arm64.tar.gz
[  OK  ] DietPi-Software | tar xf go1.18.3.linux-arm64.tar.gz --one-top-level=/usr/local
[  OK  ] DietPi-Software | rm go1.18.3.linux-arm64.tar.gz
[  OK  ] DietPi-Software | mkdir -p /mnt/dietpi_userdata/go/bin /mnt/dietpi_userdata/go/pkg /mnt/dietpi_userdata/go/src

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[UnRAR]]: unarchiver for .rar files

[ INFO ] DietPi-Software | APT install for: unrar, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
unrar is already the newest version (1:6.1.7-2).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: unrar

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[samba server]]Samba Server: Feature-rich SMB/CIFS server

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

 [[nginx]]

[[mariaDB]]

[[sqlite]]

[[php]]
 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing PHP Composer: Package manager for PHP

[  OK  ] DietPi-Software | curl -sSfL https://getcomposer.org/composer-stable.phar -o /usr/local/bin/composer
[  OK  ] DietPi-Software | chmod +x /usr/local/bin/composer

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
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: python3
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[ INFO ] DietPi-Software | Updating file: /usr/local/bin/youtube-dl
[  OK  ] DietPi-Software | mv youtube-dl /usr/local/bin/youtube-dl
[  OK  ] DietPi-Software | chmod +x /usr/local/bin/youtube-dl
[  OK  ] DietPi-Software | sed -i 1s/python$/python3/ /usr/local/bin/youtube-dl

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing AdGuard Home: powerful network-wide ads & trackers blocking DNS server

[ INFO ] DietPi-Software | AdGuard Home executable "/mnt/dietpi_userdata/adguardhome/AdGuardHome" already exists. Download and install steps will be skipped.
 - If you want to update AdGuard Home, please use the internal updater from web UI.
 - If you need to reinstall (e.g. broken instance), please manually remove the executable "/mnt/dietpi_userdata/adguardhome/AdGuardHome" and rerun "dietpi-software (re)install 126".
[ INFO ] DietPi-Software | APT install for: apache2-utils, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
apache2-utils is already the newest version (2.4.54-2).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: apache2-utils
[  OK  ] DietPi-Software | Verifying user "adguardhome" to run AdGuard Home
[  OK  ] DietPi-Software | usermod -d /mnt/dietpi_userdata/adguardhome -s /usr/sbin/nologin adguardhome
[  OK  ] DietPi-Software | chown -R adguardhome:adguardhome /mnt/dietpi_userdata/adguardhome
[  OK  ] DietPi-Software | chmod 0755 /mnt/dietpi_userdata/adguardhome/AdGuardHome
[  OK  ] DietPi-Software | chmod 0600 /mnt/dietpi_userdata/adguardhome/AdGuardHome.yaml

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Wordpress: website blog and publishing platform

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | curl -sSfL https://wordpress.org/latest.tar.gz -o latest.tar.gz
[  OK  ] DietPi-Software | tar xf latest.tar.gz --one-top-level=/var/www
[  OK  ] DietPi-Software | rm latest.tar.gz
[  OK  ] DietPi-Software | chown -R www-data:www-data /var/www/wordpress
[ INFO ] DietPi-Create_MySQL_DB | MariaDB database wordpress already exists. Aborting...

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Grafana: platform for analytics and monitoring

[  OK  ] DietPi-Software | Checking URL: https://packages.grafana.com/gpg.key
[  OK  ] DietPi-Software | eval curl -sSfL 'https://packages.grafana.com/gpg.key' | gpg --dearmor -o /etc/apt/trusted.gpg.d/dietpi-grafana.gpg --yes
[  OK  ] DietPi-Software | eval echo 'deb https://packages.grafana.com/oss/deb/ stable main' > /etc/apt/sources.list.d/grafana.list
[ INFO ] DietPi-Software | APT update, please wait...
Hit:1 https://packages.grafana.com/oss/deb stable InRelease
Hit:2 https://download.mono-project.com/repo/debian buster InRelease
Hit:3 https://downloads.plex.tv/repo/deb public InRelease
Hit:4 https://download.zerotier.com/debian/bookworm bookworm InRelease
Hit:5 https://deb.debian.org/debian bookworm InRelease
Get:6 https://archive.raspberrypi.org/debian bullseye InRelease [23.7 kB]
Hit:7 https://deb.debian.org/debian bookworm-updates InRelease
Hit:8 https://deb.debian.org/debian-security bookworm-security InRelease
Hit:9 https://deb.debian.org/debian bookworm-backports InRelease
Get:10 https://archive.raspberrypi.org/debian bullseye/main arm64 Packages [281 kB]
Fetched 305 kB in 4s (70.8 kB/s)
Reading package lists...
[  OK  ] DietPi-Software | APT update
[ INFO ] DietPi-Software | APT install for: grafana, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
grafana is already the newest version (9.0.2).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: grafana
[  OK  ] DietPi-Software | systemctl stop grafana-server
[ INFO ] DietPi-Software | Removing obsolete SysV grafana-server service
[  OK  ] DietPi-Software | update-rc.d grafana-server remove
[ INFO ] DietPi-Software | Existing database/plugin directory /mnt/dietpi_userdata/grafana found. Will not overwrite...
[  OK  ] DietPi-Software | rm -Rf /var/lib/grafana
[  OK  ] DietPi-Software | ln -s /mnt/dietpi_userdata/grafana /var/lib/grafana
[  OK  ] DietPi-Software | Current setting in /etc/grafana/grafana.ini will be preserved: admin_password = ************
[  OK  ] DietPi-Software | Current setting in /etc/grafana/grafana.ini will be preserved: http_port = 3001

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Plex Media Server: web interface media streaming server

[  OK  ] DietPi-Software | Checking URL: https://downloads.plex.tv/plex-keys/PlexSign.key
[  OK  ] DietPi-Software | eval curl -sSfL 'https://downloads.plex.tv/plex-keys/PlexSign.key' | gpg --dearmor -o /etc/apt/trusted.gpg.d/dietpi-plexmediaserver.gpg --yes
[  OK  ] DietPi-Software | eval echo 'deb https://downloads.plex.tv/repo/deb/ public main' > /etc/apt/sources.list.d/plexmediaserver.list
[ INFO ] DietPi-Software | APT update, please wait...
Hit:1 https://deb.debian.org/debian bookworm InRelease
Hit:2 https://deb.debian.org/debian bookworm-updates InRelease
Hit:3 https://download.zerotier.com/debian/bookworm bookworm InRelease
Hit:4 https://download.mono-project.com/repo/debian buster InRelease
Hit:5 https://downloads.plex.tv/repo/deb public InRelease
Hit:6 https://deb.debian.org/debian-security bookworm-security InRelease
Hit:7 https://packages.grafana.com/oss/deb stable InRelease
Hit:8 https://deb.debian.org/debian bookworm-backports InRelease
Hit:9 https://archive.raspberrypi.org/debian bullseye InRelease
Reading package lists...
[  OK  ] DietPi-Software | APT update
[ INFO ] DietPi-Software | APT install for: plexmediaserver, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
plexmediaserver is already the newest version (1.27.2.5929-a806c5905).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: plexmediaserver
[  OK  ] DietPi-Software | systemctl stop plexmediaserver
[  OK  ] DietPi-Software | Verifying user "plex" to run Plex Media Server
[  OK  ] DietPi-Software | usermod -g dietpi -aG plex,video,render -d /var/lib/plexmediaserver -s /usr/sbin/nologin plex
[  OK  ] DietPi-Software | eval echo -e '[Service]\nGroup=' > /etc/systemd/system/plexmediaserver.service.d/dietpi-group.conf

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing rTorrent: BitTorrent server with rutorrent web interface

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://github.com/Novik/ruTorrent/archive/v3.10.tar.gz
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://github.com/Novik/ruTorrent/archive/v3.10.tar.gz -o v3.10.tar.gz
[ INFO ] DietPi-Software | APT install for: rtorrent mediainfo, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
mediainfo is already the newest version (22.06-1).
rtorrent is already the newest version (0.9.8-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: rtorrent mediainfo
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[  OK  ] DietPi-Software | tar xf v3.10.tar.gz
[  OK  ] DietPi-Software | rm v3.10.tar.gz
[  OK  ] DietPi-Software | mv ruTorrent-3.10/conf/config.php ruTorrent-3.10/conf/config.php.example
[  OK  ] DietPi-Software | cp -a /var/www/rutorrent/conf/config.php ruTorrent-3.10/conf/config.php
[  OK  ] DietPi-Software | mv ruTorrent-3.10/conf/access.ini ruTorrent-3.10/conf/access.ini.example
[  OK  ] DietPi-Software | cp -a /var/www/rutorrent/conf/access.ini ruTorrent-3.10/conf/access.ini
[  OK  ] DietPi-Software | mv ruTorrent-3.10/conf/plugins.ini ruTorrent-3.10/conf/plugins.ini.example
[  OK  ] DietPi-Software | cp -a /var/www/rutorrent/conf/plugins.ini ruTorrent-3.10/conf/plugins.ini
[  OK  ] DietPi-Software | rm -R /var/www/rutorrent
[  OK  ] DietPi-Software | mv ruTorrent-3.10 /var/www/rutorrent
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | curl -sSfL https://github.com/chocolatkey/DarkBetter/archive/master.tar.gz -o master.tar.gz
[  OK  ] DietPi-Software | tar xf master.tar.gz
[  OK  ] DietPi-Software | rm master.tar.gz
[  OK  ] DietPi-Software | rm -R /var/www/rutorrent/plugins/theme/themes/DarkBetter
[  OK  ] DietPi-Software | mv DarkBetter-master /var/www/rutorrent/plugins/theme/themes/DarkBetter
[  OK  ] DietPi-Software | chmod 0400 /etc/.rutorrent-htaccess
[  OK  ] DietPi-Software | chown www-data:www-data /etc/.rutorrent-htaccess
[  OK  ] DietPi-Software | Desired setting in /var/www/rutorrent/conf/config.php was already set: 	$scgi_port = 0;
[  OK  ] DietPi-Software | Desired setting in /var/www/rutorrent/conf/config.php was already set: 	$scgi_host = "unix:///mnt/dietpi_userdata/downloads/.session/rpc.socket";
[  OK  ] DietPi-Software | Desired setting in /var/www/rutorrent/conf/config.php was already set: 		"curl"	=> "/usr/bin/curl",
[  OK  ] DietPi-Software | Verifying user "rtorrent" to run rTorrent
[  OK  ] DietPi-Software | usermod -g dietpi -d /mnt/dietpi_userdata/rtorrent -s /usr/sbin/nologin rtorrent
[  OK  ] DietPi-Software | Desired setting in /mnt/dietpi_userdata/rtorrent/.rtorrent.rc was already set: system.daemon.set = true
[  OK  ] DietPi-Software | sed -i /^[[:blank:]]*network.scgi.open_port[[:blank:]=]/d /mnt/dietpi_userdata/rtorrent/.rtorrent.rc
[  OK  ] DietPi-Software | Desired setting in /mnt/dietpi_userdata/rtorrent/.rtorrent.rc was already set: network.scgi.open_local = /mnt/dietpi_userdata/downloads/.session/rpc.socket
[  OK  ] DietPi-Software | Desired setting in /mnt/dietpi_userdata/rtorrent/.rtorrent.rc was already set: execute.nothrow = chmod,666,/mnt/dietpi_userdata/downloads/.session/rpc.socket
[  OK  ] DietPi-Software | chown -R rtorrent:root /mnt/dietpi_userdata/rtorrent /mnt/dietpi_userdata/downloads/.session
[  OK  ] DietPi-Software | chown -R www-data:root /var/www/rutorrent/share
[  OK  ] DietPi-Software | chown root:root /var/www/rutorrent/share/.htaccess

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Aria2: Download manager with web interface

[ INFO ] DietPi-Software | APT install for: aria2, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
aria2 is already the newest version (1.36.0-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: aria2
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | curl -sSfL https://github.com/ziahamza/webui-aria2/archive/master.tar.gz -o master.tar.gz
[  OK  ] DietPi-Software | tar xf master.tar.gz
[  OK  ] DietPi-Software | rm master.tar.gz
[  OK  ] DietPi-Software | rm -R /var/www/aria2
[  OK  ] DietPi-Software | mv webui-aria2-master /var/www/aria2
[  OK  ] DietPi-Software | Verifying user "aria2" to run Aria2
[  OK  ] DietPi-Software | usermod -g dietpi -d /mnt/dietpi_userdata/aria2 -s /usr/sbin/nologin aria2
[  OK  ] DietPi-Software | chown -R aria2:root /mnt/dietpi_userdata/aria2 /mnt/dietpi_userdata/downloads/aria2.session
[  OK  ] DietPi-Software | chown aria2:dietpi /var/log/aria2.log
[  OK  ] DietPi-Software | chmod 600 /mnt/dietpi_userdata/aria2/aria2.conf

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Medusa: Automatic Video Library Manager for TV Shows

[ INFO ] DietPi-Software | Medusa install dir "/mnt/dietpi_userdata/medusa" already exists. Download and install steps will be skipped.
 - If you want to update Medusa, please use the internal updater from web UI.
 - If you need to reinstall (e.g. broken instance), please manually backup your config files+data, remove the install dir and rerun "dietpi-software (re)install 116".
[ INFO ] DietPi-Software | APT install for: mediainfo python3, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
mediainfo is already the newest version (22.06-1).
python3 is already the newest version (3.10.4-1+b1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: mediainfo python3
[  OK  ] DietPi-Software | Verifying user "medusa" to run Medusa
[  OK  ] DietPi-Software | usermod -g dietpi -d /mnt/dietpi_userdata/medusa -s /usr/sbin/nologin medusa
[  OK  ] DietPi-Software | cp /mnt/dietpi_userdata/medusa/runscripts/init.systemd /etc/systemd/system/medusa.service
[  OK  ] DietPi-Software | Added setting StartLimitIntervalSec=600 to /etc/systemd/system/medusa.service after line [Unit]
[  OK  ] DietPi-Software | Added setting StartLimitBurst=3 to /etc/systemd/system/medusa.service after line StartLimitIntervalSec=600
[  OK  ] DietPi-Software | sed -i /^[[:blank:]]*Group=/d /etc/systemd/system/medusa.service
[  OK  ] DietPi-Software | Setting in /etc/systemd/system/medusa.service adjusted: ExecStart=/usr/bin/python3 /mnt/dietpi_userdata/medusa/start.py -q --nolaunch --datadir=/mnt/dietpi_userdata/medusa
[  OK  ] DietPi-Software | chown -R medusa:dietpi /mnt/dietpi_userdata/medusa

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Chromium: web browser for desktop or autostart

[ INFO ] DietPi-Software | APT install for: chromium-browser chromium-codecs-ffmpeg-extra libpam-systemd, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
libpam-systemd is already the newest version (251.2-7).
chromium-browser is already the newest version (101.0.4951.57-rpt2).
chromium-codecs-ffmpeg-extra is already the newest version (101.0.4951.57-rpt2).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: chromium-browser chromium-codecs-ffmpeg-extra libpam-systemd
[ SUB1 ] DietPi-Set_hardware > rpi-codec (enable)
[  OK  ] DietPi-Set_hardware | Desired setting in /boot/config.txt was already set: dtoverlay=rpivid-v4l2
[  OK  ] rpi-codec enable | Completed
[  OK  ] DietPi-Software | chmod +x /var/lib/dietpi/dietpi-software/installed/chromium-autostart.sh

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Sonarr: Automatically download TV shows

[  OK  ] DietPi-Software | apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 2009837CBFFD68F45BC180471F4F90DE2A9B4BF8
[  OK  ] DietPi-Software | eval echo 'deb https://apt.sonarr.tv/debian/ buster main' > /etc/apt/sources.list.d/sonarr.list
[ INFO ] DietPi-Software | APT update, please wait...
Hit:1 https://download.mono-project.com/repo/debian buster InRelease
Hit:2 https://deb.debian.org/debian bookworm InRelease
Hit:3 https://packages.grafana.com/oss/deb stable InRelease
Hit:4 https://downloads.plex.tv/repo/deb public InRelease
Hit:5 https://deb.debian.org/debian bookworm-updates InRelease
Hit:6 https://download.zerotier.com/debian/bookworm bookworm InRelease
Hit:7 https://archive.raspberrypi.org/debian bullseye InRelease
Hit:8 https://deb.debian.org/debian-security bookworm-security InRelease
Hit:9 https://deb.debian.org/debian bookworm-backports InRelease
Get:10 https://apt.sonarr.tv/debian buster InRelease [17.6 kB]
Get:11 https://apt.sonarr.tv/debian buster/main arm64 Packages [2571 B]
Fetched 20.2 kB in 4s (4553 B/s)
Reading package lists...
W: https://apt.sonarr.tv/debian/dists/buster/InRelease: Key is stored in legacy trusted.gpg keyring (/etc/apt/trusted.gpg), see the DEPRECATION section in apt-key(8) for details.
[  OK  ] DietPi-Software | APT update
[  OK  ] DietPi-Software | eval debconf-set-selections <<< 'sonarr sonarr/owning_group string dietpi'
[  OK  ] DietPi-Software | eval debconf-set-selections <<< 'sonarr sonarr/config_directory string /mnt/dietpi_userdata/sonarr'
[ INFO ] DietPi-Software | APT install for: sonarr mediainfo, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
mediainfo is already the newest version (22.06-1).
The following NEW packages will be installed:
  sonarr
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 8910 kB of archives.
After this operation, 35.0 MB of additional disk space will be used.
Get:1 https://apt.sonarr.tv/debian buster/main arm64 sonarr all 3.0.8 [8910 kB]
debconf: delaying package configuration, since apt-utils is not installed
Fetched 8910 kB in 6s (1475 kB/s)
                                 Selecting previously unselected package sonarr.
(Reading database ... 53131 files and directories currently installed.)
Preparing to unpack .../archives/sonarr_3.0.8_all.deb ...
Unpacking sonarr (3.0.8) ...
Setting up sonarr (3.0.8) ...
Adding system user `sonarr' (UID 109) ...
Adding new user `sonarr' (UID 109) with group `dietpi' ...
Not creating home directory `/home/sonarr'.
Created symlink /etc/systemd/system/multi-user.target.wants/sonarr.service → /lib/systemd/system/sonarr.service.
[  OK  ] DietPi-Software | APT install for: sonarr mediainfo
[  OK  ] DietPi-Software | systemctl stop sonarr
[  OK  ] DietPi-Software | Verifying user "sonarr" to run Sonarr
[  OK  ] DietPi-Software | usermod -g dietpi -d /mnt/dietpi_userdata/sonarr -s /usr/sbin/nologin sonarr
[  OK  ] DietPi-Software | rm -Rf /mnt/dietpi_userdata/sonarr/logs*
[  OK  ] DietPi-Software | ln -s /var/log/sonarr /mnt/dietpi_userdata/sonarr/logs
[  OK  ] DietPi-Software | ln -s /var/log/sonarr/logs.db /mnt/dietpi_userdata/sonarr/logs.db
[  OK  ] DietPi-Software | ln -s /var/log/sonarr/logs.db-shm /mnt/dietpi_userdata/sonarr/logs.db-shm
[  OK  ] DietPi-Software | ln -s /var/log/sonarr/logs.db-wal /mnt/dietpi_userdata/sonarr/logs.db-wal
[  OK  ] DietPi-Software | chown -R sonarr:dietpi /mnt/dietpi_userdata/sonarr /usr/lib/sonarr

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Radarr: Automatically download movies

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://github.com/Radarr/Radarr/releases/download/v4.1.0.6175/Radarr.master.4.1.0.6175.linux-core-arm64.tar.gz
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://github.com/Radarr/Radarr/releases/download/v4.1.0.6175/Radarr.master.4.1.0.6175.linux-core-arm64.tar.gz -o Radarr.master.4.1.0.6175.linux-core-arm64.tar.gz
[ INFO ] DietPi-Software | APT install for: mediainfo libicu71, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
libicu71 is already the newest version (71.1-3).
libicu71 set to manually installed.
mediainfo is already the newest version (22.06-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: mediainfo libicu71
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[  OK  ] DietPi-Software | tar xf Radarr.master.4.1.0.6175.linux-core-arm64.tar.gz
[  OK  ] DietPi-Software | rm Radarr.master.4.1.0.6175.linux-core-arm64.tar.gz
[  OK  ] DietPi-Software | mv Radarr /opt/radarr
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/radarr
[  OK  ] DietPi-Software | Verifying user "radarr" to run Radarr
[  OK  ] DietPi-Software | useradd -rMN -g dietpi -d /mnt/dietpi_userdata/radarr -s /usr/sbin/nologin radarr
[  OK  ] DietPi-Software | rm -Rf /mnt/dietpi_userdata/radarr/logs*
[  OK  ] DietPi-Software | ln -s /var/log/radarr /mnt/dietpi_userdata/radarr/logs
[  OK  ] DietPi-Software | ln -s /var/log/radarr/logs.db /mnt/dietpi_userdata/radarr/logs.db
[  OK  ] DietPi-Software | ln -s /var/log/radarr/logs.db-shm /mnt/dietpi_userdata/radarr/logs.db-shm
[  OK  ] DietPi-Software | ln -s /var/log/radarr/logs.db-wal /mnt/dietpi_userdata/radarr/logs.db-wal
[  OK  ] DietPi-Software | chown -R radarr:dietpi /mnt/dietpi_userdata/radarr /opt/radarr

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Lidarr: Automatically download music

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://github.com/Lidarr/Lidarr/releases/download/v1.0.2.2592/Lidarr.master.1.0.2.2592.linux-core-arm64.tar.gz
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://github.com/Lidarr/Lidarr/releases/download/v1.0.2.2592/Lidarr.master.1.0.2.2592.linux-core-arm64.tar.gz -o Lidarr.master.1.0.2.2592.linux-core-arm64.tar.gz
[ INFO ] DietPi-Software | APT install for: mediainfo libicu71, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
libicu71 is already the newest version (71.1-3).
mediainfo is already the newest version (22.06-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: mediainfo libicu71
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[  OK  ] DietPi-Software | tar xf Lidarr.master.1.0.2.2592.linux-core-arm64.tar.gz
[  OK  ] DietPi-Software | rm Lidarr.master.1.0.2.2592.linux-core-arm64.tar.gz
[  OK  ] DietPi-Software | mv Lidarr /opt/lidarr
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/lidarr
[  OK  ] DietPi-Software | Verifying user "lidarr" to run Lidarr
[  OK  ] DietPi-Software | useradd -rMN -g dietpi -d /mnt/dietpi_userdata/lidarr -s /usr/sbin/nologin lidarr
[  OK  ] DietPi-Software | rm -Rf /mnt/dietpi_userdata/lidarr/logs*
[  OK  ] DietPi-Software | ln -s /var/log/lidarr /mnt/dietpi_userdata/lidarr/logs
[  OK  ] DietPi-Software | ln -s /var/log/lidarr/logs.db /mnt/dietpi_userdata/lidarr/logs.db
[  OK  ] DietPi-Software | ln -s /var/log/lidarr/logs.db-shm /mnt/dietpi_userdata/lidarr/logs.db-shm
[  OK  ] DietPi-Software | ln -s /var/log/lidarr/logs.db-wal /mnt/dietpi_userdata/lidarr/logs.db-wal
[  OK  ] DietPi-Software | chown -R lidarr:dietpi /mnt/dietpi_userdata/lidarr /opt/lidarr

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Bazarr: Automatically download subtitles

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | curl -sSfL https://github.com/morpheus65535/bazarr/releases/latest/download/bazarr.zip -o bazarr.zip
[  OK  ] DietPi-Software | unzip -o bazarr.zip -d/opt/bazarr
[  OK  ] DietPi-Software | rm bazarr.zip
[ INFO ] DietPi-Software | APT install for: gcc, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
gcc is already the newest version (4:11.2.0-2).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: gcc
[  OK  ] DietPi-Software | cd /opt/bazarr
[ INFO ] DietPi-Software | pip3 install --no-cache-dir -Ur requirements.txt, please wait...
Requirement already satisfied: setuptools in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 1)) (63.1.0)
Collecting lxml>=4.3.0
  Downloading lxml-4.9.1-cp310-cp310-manylinux_2_17_aarch64.manylinux2014_aarch64.manylinux_2_24_aarch64.whl (6.6 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 6.6/6.6 MB 1.9 MB/s eta 0:00:00
Collecting numpy>=1.12.0
  Downloading numpy-1.23.1-cp310-cp310-manylinux_2_17_aarch64.manylinux2014_aarch64.whl (13.9 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 13.9/13.9 MB 6.7 MB/s eta 0:00:00
Collecting webrtcvad-wheels>=2.0.10
  Downloading webrtcvad-wheels-2.0.10.post2.tar.gz (67 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 68.0/68.0 kB 10.8 MB/s eta 0:00:00
  Preparing metadata (setup.py): started
  Preparing metadata (setup.py): finished with status 'done'
Building wheels for collected packages: webrtcvad-wheels
  Building wheel for webrtcvad-wheels (setup.py): started
  Building wheel for webrtcvad-wheels (setup.py): finished with status 'done'
  Created wheel for webrtcvad-wheels: filename=webrtcvad_wheels-2.0.10.post2-cp310-cp310-linux_aarch64.whl size=72452 sha256=3dba33df984b37cbef32d3ac1ef27a7e4b416f965f73aa7b604b0fdc1f56b6ac
  Stored in directory: /tmp/pip-ephem-wheel-cache-7cxhw8mp/wheels/6a/1f/96/9ec7e8a9f239888d3c5b5b84cd8fc793d2a0bebccbf9eb0f5d
Successfully built webrtcvad-wheels
Installing collected packages: webrtcvad-wheels, numpy, lxml
Successfully installed lxml-4.9.1 numpy-1.23.1 webrtcvad-wheels-2.0.10.post2
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv
[  OK  ] DietPi-Software | pip3 install --no-cache-dir -Ur requirements.txt
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/bazarr
[  OK  ] DietPi-Software | Verifying user "bazarr" to run Bazarr
[  OK  ] DietPi-Software | useradd -rMN -g dietpi -d /mnt/dietpi_userdata/bazarr -s /usr/sbin/nologin bazarr
[  OK  ] DietPi-Software | rm -Rf /mnt/dietpi_userdata/bazarr/log
[  OK  ] DietPi-Software | ln -s /var/log/bazarr /mnt/dietpi_userdata/bazarr/log
[  OK  ] DietPi-Software | chown -R bazarr:dietpi /mnt/dietpi_userdata/bazarr /opt/bazarr
[  OK  ] DietPi-Software | systemctl daemon-reload
[  OK  ] DietPi-Software | Starting Bazarr to pre-create config file in max 25 seconds
[  OK  ] DietPi-Software | systemctl stop bazarr
[ INFO ] DietPi-Software | Bazarr config file got created after 4 seconds
[  OK  ] DietPi-Software | systemctl daemon-reload
[  OK  ] DietPi-Software | Starting Bazarr to pre-create config file in max 25 seconds
[  OK  ] DietPi-Software | systemctl stop sonarr
[ INFO ] DietPi-Software | Bazarr config file got created after 22 seconds
[  OK  ] DietPi-Software | sed -i /\[sonarr\]/,/^$/s/^ip = .*$/ip = 127.0.0.1/ /mnt/dietpi_userdata/bazarr/config/config.ini
[  OK  ] DietPi-Software | sed -i /\[sonarr\]/,/^$/s/^port = .*$/port = 8989/ /mnt/dietpi_userdata/bazarr/config/config.ini
[  OK  ] DietPi-Software | sed -i /\[sonarr\]/,/^$/s/^base_url = .*$/base_url = \// /mnt/dietpi_userdata/bazarr/config/config.ini
[  OK  ] DietPi-Software | sed -i /\[sonarr\]/,/^$/s/^apikey = .*$/apikey = 6528be49014044b896cd8782856ed5d5/ /mnt/dietpi_userdata/bazarr/config/config.ini
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/bazarr/config/config.ini adjusted: use_sonarr = True
[  OK  ] DietPi-Software | systemctl daemon-reload
[  OK  ] DietPi-Software | Starting Bazarr to pre-create config file in max 25 seconds
[  OK  ] DietPi-Software | systemctl stop radarr
[FAILED] DietPi-Software | Waiting for Bazarr config file failed, skipping pre-configuration

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Tautulli: monitoring and tracking tool for Plex

[  OK  ] DietPi-Software | Checking URL: https://github.com/Tautulli/Tautulli.git
[ INFO ] DietPi-Software | G_THREAD_START_0 | git clone --depth 1 https://github.com/Tautulli/Tautulli.git
[ INFO ] DietPi-Software | APT install for: python3-pkg-resources, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
python3-pkg-resources is already the newest version (59.6.0-1.2).
python3-pkg-resources set to manually installed.
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: python3-pkg-resources
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[  OK  ] DietPi-Software | mv Tautulli /opt/tautulli
[  OK  ] DietPi-Software | Verifying user "tautulli" to run Tautulli
[  OK  ] DietPi-Software | useradd -rMU -d /mnt/dietpi_userdata/tautulli -s /usr/sbin/nologin tautulli
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/tautulli
[  OK  ] DietPi-Software | chown -R tautulli:tautulli /opt/tautulli /mnt/dietpi_userdata/tautulli

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Jackett: API support for your torrent trackers

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://github.com/Jackett/Jackett/releases/download/v0.20.1300/Jackett.Binaries.LinuxARM64.tar.gz
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://github.com/Jackett/Jackett/releases/download/v0.20.1300/Jackett.Binaries.LinuxARM64.tar.gz -o Jackett.Binaries.LinuxARM64.tar.gz
[ INFO ] DietPi-Software | APT install for: libicu71, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
libicu71 is already the newest version (71.1-3).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: libicu71
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[  OK  ] DietPi-Software | tar xf Jackett.Binaries.LinuxARM64.tar.gz
[  OK  ] DietPi-Software | rm Jackett.Binaries.LinuxARM64.tar.gz
[  OK  ] DietPi-Software | mv Jackett /opt/jackett
[  OK  ] DietPi-Software | Verifying user "jackett" to run Jackett
[  OK  ] DietPi-Software | useradd -rMU -d /opt/jackett -s /usr/sbin/nologin jackett
[  OK  ] DietPi-Software | chown -R jackett:jackett /opt/jackett

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing NZBGet: NZB download manager

[  OK  ] DietPi-Software | curl -sSfL https://nzbget.net/download/nzbget-latest-bin-linux.run -o package.run
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/nzbget
[ INFO ] DietPi-Software | dash package.run --destdir /mnt/dietpi_userdata/nzbget, please wait...
Installer for nzbget-21.1
Verifying package...
Checking system...
CPU-Architecture: aarch64
Unpacking...
Configuring...
  Free memory detected: 3459 MB
  Activating article cache (ArticleCache=100)
  Increasing write buffer (WriteBuffer=1024)
  Increasing par repair buffer (ParBuffer=100)
  Activating direct rename (DirectRename=yes)
  CPU speed detected: 432 BogoMIPS
  Disabling download during par check/repair (ParPauseQueue=yes)
  Disabling download during unpack (UnpackPauseQueue=yes)
  Disabling download during post-processing (ScriptPauseQueue=yes)
Installation completed

Quick help (from nzbget-directory):
   ./nzbget -s        - start nzbget in console mode
   ./nzbget -D        - start nzbget in daemon mode (in background)
   ./nzbget -C        - connect to background process
   ./nzbget -Q        - stop background process
   ./nzbget -h        - help screen with all commands

Successfully installed into /mnt/dietpi_userdata/nzbget
Web-interface is on http://localhost:6789 (login:nzbget, password:tegbzn6789)
For support please visit http://nzbget.net/forum
[  OK  ] DietPi-Software | dash package.run --destdir /mnt/dietpi_userdata/nzbget
[  OK  ] DietPi-Software | rm package.run
[  OK  ] DietPi-Software | Verifying user "nzbget" to run NZBGet
[  OK  ] DietPi-Software | useradd -rMN -g dietpi -d /mnt/dietpi_userdata/nzbget -s /usr/sbin/nologin nzbget
[  OK  ] DietPi-Software | chown -R nzbget:root /mnt/dietpi_userdata/nzbget
[  OK  ] DietPi-Software | chmod 0600 /mnt/dietpi_userdata/nzbget/nzbget.conf
[  OK  ] DietPi-Software | /mnt/dietpi_userdata/nzbget/nzbget.conf: backup to /mnt/dietpi_userdata/nzbget/nzbget.conf.bak_120722_0
[ INFO ] DietPi-Software | For a full list of backup items, please see /var/tmp/dietpi/logs/G_BACKUP_FP.db
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: MainDir=/mnt/dietpi_userdata/downloads
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: DestDir=/mnt/dietpi_userdata/downloads/complete
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: LogFile=/var/log/nzbget.log
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: ControlUsername=admin
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: ControlPassword=******
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: UMask=0002
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: Server1.Cipher=RC4-MD5
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: CrcCheck=no
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: ParScan=limited
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: ParThreads=4
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: DebugTarget=none
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: CrashTrace=no
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: DetailTarget=none
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: ParBuffer=384
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: ArticleCache=384
[  OK  ] DietPi-Software | Setting in /mnt/dietpi_userdata/nzbget/nzbget.conf adjusted: WriteBuffer=384

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Prowlarr: Indexer Manager & Proxy for PVR

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://github.com/Prowlarr/Prowlarr/releases/download/v0.4.2.1879/Prowlarr.develop.0.4.2.1879.linux-core-arm64.tar.gz
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://github.com/Prowlarr/Prowlarr/releases/download/v0.4.2.1879/Prowlarr.develop.0.4.2.1879.linux-core-arm64.tar.gz -o Prowlarr.develop.0.4.2.1879.linux-core-arm64.tar.gz
[ INFO ] DietPi-Software | APT install for: libicu71, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
libicu71 is already the newest version (71.1-3).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT install for: libicu71
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[  OK  ] DietPi-Software | tar xf Prowlarr.develop.0.4.2.1879.linux-core-arm64.tar.gz
[  OK  ] DietPi-Software | rm Prowlarr.develop.0.4.2.1879.linux-core-arm64.tar.gz
[  OK  ] DietPi-Software | mv Prowlarr /opt/prowlarr
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/prowlarr
[  OK  ] DietPi-Software | Verifying user "prowlarr" to run Prowlarr
[  OK  ] DietPi-Software | useradd -rMN -g dietpi -d /mnt/dietpi_userdata/prowlarr -s /usr/sbin/nologin prowlarr
[  OK  ] DietPi-Software | chown -R prowlarr:dietpi /mnt/dietpi_userdata/prowlarr /opt/prowlarr

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing HTPC Manager: Manage your HTPC from anywhere

[  OK  ] DietPi-Software | Checking URL: https://github.com/HTPC-Manager/HTPC-Manager.git
[ INFO ] DietPi-Software | APT install for: libffi-dev libssl-dev zlib1g-dev libjpeg-dev, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
libssl-dev is already the newest version (3.0.4-2).
zlib1g-dev is already the newest version (1:1.2.11.dfsg-4).
zlib1g-dev set to manually installed.
The following additional packages will be installed:
  libjpeg62-turbo-dev
The following NEW packages will be installed:
  libffi-dev libjpeg-dev libjpeg62-turbo-dev
0 upgraded, 3 newly installed, 0 to remove and 0 not upgraded.
Need to get 405 kB of archives.
After this operation, 1150 kB of additional disk space will be used.
Get:1 https://deb.debian.org/debian bookworm/main arm64 libffi-dev arm64 3.4.2-4 [57.7 kB]
Get:2 https://deb.debian.org/debian bookworm/main arm64 libjpeg62-turbo-dev arm64 1:2.1.2-1 [272 kB]
Get:3 https://deb.debian.org/debian bookworm/main arm64 libjpeg-dev arm64 1:2.1.2-1 [74.7 kB]
debconf: delaying package configuration, since apt-utils is not installed
Fetched 405 kB in 1s (631 kB/s)
                               Selecting previously unselected package libffi-dev:arm64.
(Reading database ... 53360 files and directories currently installed.)
Preparing to unpack .../libffi-dev_3.4.2-4_arm64.deb ...
Unpacking libffi-dev:arm64 (3.4.2-4) ...
Selecting previously unselected package libjpeg62-turbo-dev:arm64.
Preparing to unpack .../libjpeg62-turbo-dev_1%3a2.1.2-1_arm64.deb ...
Unpacking libjpeg62-turbo-dev:arm64 (1:2.1.2-1) ...
Selecting previously unselected package libjpeg-dev:arm64.
Preparing to unpack .../libjpeg-dev_1%3a2.1.2-1_arm64.deb ...
Unpacking libjpeg-dev:arm64 (1:2.1.2-1) ...
Setting up libffi-dev:arm64 (3.4.2-4) ...
Setting up libjpeg62-turbo-dev:arm64 (1:2.1.2-1) ...
Setting up libjpeg-dev:arm64 (1:2.1.2-1) ...
[  OK  ] DietPi-Software | APT install for: libffi-dev libssl-dev zlib1g-dev libjpeg-dev
[ INFO ] DietPi-Software | git clone --depth 1 https://github.com/HTPC-Manager/HTPC-Manager.git, please wait...
Cloning into 'HTPC-Manager'...
[  OK  ] DietPi-Software | git clone --depth 1 https://github.com/HTPC-Manager/HTPC-Manager.git
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/htpc-manager
[  OK  ] DietPi-Software | cp -a HTPC-Manager/. /mnt/dietpi_userdata/htpc-manager/
[  OK  ] DietPi-Software | rm -R HTPC-Manager
[  OK  ] DietPi-Software | cd /mnt/dietpi_userdata/htpc-manager
[ INFO ] DietPi-Software | git reset --hard origin, please wait...
HEAD is now at 15ec6d9 Release 2021-07-27 (#43)
[  OK  ] DietPi-Software | git reset --hard origin
[ INFO ] DietPi-Software | git clean -dxfe /userdata, please wait...
[  OK  ] DietPi-Software | git clean -dxfe /userdata
[ INFO ] DietPi-Software | pip3 install --no-cache-dir -Ur requirements.txt, please wait...
Collecting ssdp
  Downloading ssdp-1.1.0-py2.py3-none-any.whl (4.3 kB)
Collecting jaraco.collections
  Downloading jaraco.collections-3.5.1-py3-none-any.whl (10 kB)
Requirement already satisfied: six in /usr/lib/python3/dist-packages (from -r requirements.txt (line 4)) (1.16.0)
Collecting apscheduler
  Downloading APScheduler-3.9.1-py2.py3-none-any.whl (59 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 59.5/59.5 kB 1.1 MB/s eta 0:00:00
Collecting pypi-xmlrpc
  Downloading pypi-xmlrpc-2020.12.3.tar.gz (2.0 kB)
  Preparing metadata (setup.py): started
  Preparing metadata (setup.py): finished with status 'done'
Collecting colorama
  Downloading colorama-0.4.5-py2.py3-none-any.whl (16 kB)
Collecting formencode
  Downloading FormEncode-2.0.1-py2.py3-none-any.whl (363 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 363.5/363.5 kB 825.3 kB/s eta 0:00:00
Collecting requests
  Downloading requests-2.28.1-py3-none-any.whl (62 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 62.8/62.8 kB 2.2 MB/s eta 0:00:00
Collecting requests-futures
  Downloading requests_futures-1.0.0-py2.py3-none-any.whl (7.4 kB)
Collecting mako
  Downloading Mako-1.2.1-py3-none-any.whl (78 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 78.6/78.6 kB 3.6 MB/s eta 0:00:00
Collecting tzlocal
  Downloading tzlocal-4.2-py3-none-any.whl (19 kB)
Collecting xmltodict
  Downloading xmltodict-0.13.0-py2.py3-none-any.whl (10.0 kB)
Collecting cherrypy<9.0
  Downloading CherryPy-8.9.1-py2.py3-none-any.whl (464 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 464.5/464.5 kB 2.3 MB/s eta 0:00:00
Collecting jsonrpclib-pelix
  Downloading jsonrpclib_pelix-0.4.3.2-py2.py3-none-any.whl (42 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 42.5/42.5 kB 6.1 MB/s eta 0:00:00
Requirement already satisfied: pytz in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 16)) (2022.1)
Collecting pyasn1
  Downloading pyasn1-0.4.8-py2.py3-none-any.whl (77 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 77.1/77.1 kB 5.6 MB/s eta 0:00:00
Collecting sqlobject
  Downloading SQLObject-3.9.1-py2.py3-none-any.whl (224 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 224.8/224.8 kB 1.1 MB/s eta 0:00:00
Collecting workerpool
  Downloading workerpool-0.9.4.tar.gz (5.4 kB)
  Preparing metadata (setup.py): started
  Preparing metadata (setup.py): finished with status 'done'
Requirement already satisfied: Pillow in /usr/local/lib/python3.10/dist-packages (from -r requirements.txt (line 23)) (9.2.0)
Collecting psutil>=3.0.0
  Downloading psutil-5.9.1.tar.gz (479 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 479.1/479.1 kB 1.4 MB/s eta 0:00:00
  Installing build dependencies: started
  Installing build dependencies: finished with status 'done'
  Getting requirements to build wheel: started
  Getting requirements to build wheel: finished with status 'done'
  Preparing metadata (pyproject.toml): started
  Preparing metadata (pyproject.toml): finished with status 'done'
Collecting pyopenssl
  Downloading pyOpenSSL-22.0.0-py2.py3-none-any.whl (55 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 55.8/55.8 kB 1.2 MB/s eta 0:00:00
Collecting paramiko
  Downloading paramiko-2.11.0-py2.py3-none-any.whl (212 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 212.9/212.9 kB 733.3 kB/s eta 0:00:00
Collecting pySMART>=1.0.6
  Downloading pySMART-1.1.0-py3-none-any.whl (40 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 41.0/41.0 kB 6.1 MB/s eta 0:00:00
Collecting jaraco.classes
  Downloading jaraco.classes-3.2.1-py3-none-any.whl (5.6 kB)
Collecting jaraco.text
  Downloading jaraco.text-3.8.0-py3-none-any.whl (9.7 kB)
Requirement already satisfied: setuptools>=0.7 in /usr/local/lib/python3.10/dist-packages (from apscheduler->-r requirements.txt (line 5)) (63.1.0)
Collecting click
  Downloading click-8.1.3-py3-none-any.whl (96 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 96.6/96.6 kB 6.4 MB/s eta 0:00:00
Collecting certifi>=2017.4.17
  Downloading certifi-2022.6.15-py3-none-any.whl (160 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 160.2/160.2 kB 890.3 kB/s eta 0:00:00
Requirement already satisfied: urllib3<1.27,>=1.21.1 in /usr/local/lib/python3.10/dist-packages (from requests->-r requirements.txt (line 9)) (1.26.10)
Collecting charset-normalizer<3,>=2
  Downloading charset_normalizer-2.1.0-py3-none-any.whl (39 kB)
Collecting idna<4,>=2.5
  Downloading idna-3.3-py3-none-any.whl (61 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 61.2/61.2 kB 4.3 MB/s eta 0:00:00
Requirement already satisfied: MarkupSafe>=0.9.2 in /usr/local/lib/python3.10/dist-packages (from mako->-r requirements.txt (line 11)) (2.1.1)
Collecting pytz-deprecation-shim
  Downloading pytz_deprecation_shim-0.1.0.post0-py2.py3-none-any.whl (15 kB)
Collecting PyDispatcher>=2.0.4
  Downloading PyDispatcher-2.0.5.zip (47 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 47.6/47.6 kB 3.3 MB/s eta 0:00:00
  Preparing metadata (setup.py): started
  Preparing metadata (setup.py): finished with status 'done'
Collecting cryptography>=35.0
  Downloading cryptography-37.0.4-cp36-abi3-manylinux_2_17_aarch64.manylinux2014_aarch64.manylinux_2_24_aarch64.whl (3.7 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.7/3.7 MB 2.7 MB/s eta 0:00:00
Collecting pynacl>=1.0.1
  Downloading PyNaCl-1.5.0-cp36-abi3-manylinux_2_17_aarch64.manylinux2014_aarch64.manylinux_2_24_aarch64.whl (601 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 601.7/601.7 kB 3.4 MB/s eta 0:00:00
Collecting bcrypt>=3.1.3
  Downloading bcrypt-3.2.2-cp36-abi3-manylinux_2_17_aarch64.manylinux2014_aarch64.manylinux_2_24_aarch64.whl (54 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 54.9/54.9 kB 4.1 MB/s eta 0:00:00
Collecting humanfriendly
  Downloading humanfriendly-10.0-py2.py3-none-any.whl (86 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 86.8/86.8 kB 27.0 MB/s eta 0:00:00
Collecting cffi>=1.1
  Downloading cffi-1.15.1-cp310-cp310-manylinux_2_17_aarch64.manylinux2014_aarch64.whl (449 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 449.9/449.9 kB 8.9 MB/s eta 0:00:00
Collecting more-itertools
  Downloading more_itertools-8.13.0-py3-none-any.whl (51 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 51.6/51.6 kB 27.3 MB/s eta 0:00:00
Collecting jaraco.functools
  Downloading jaraco.functools-3.5.0-py3-none-any.whl (7.0 kB)
Collecting jaraco.context>=4.1
  Downloading jaraco.context-4.1.1-py3-none-any.whl (4.4 kB)
Collecting tzdata
  Downloading tzdata-2022.1-py2.py3-none-any.whl (339 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 339.5/339.5 kB 7.3 MB/s eta 0:00:00
Collecting pycparser
  Downloading pycparser-2.21-py2.py3-none-any.whl (118 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 118.7/118.7 kB 13.4 MB/s eta 0:00:00
Building wheels for collected packages: pypi-xmlrpc, workerpool, psutil, PyDispatcher
  Building wheel for pypi-xmlrpc (setup.py): started
  Building wheel for pypi-xmlrpc (setup.py): finished with status 'done'
  Created wheel for pypi-xmlrpc: filename=pypi_xmlrpc-2020.12.3-py3-none-any.whl size=2439 sha256=335e46473f5a5b8741c827bf3cf14c4fcae45dc63652dbe70bf0a1e819cfa5fd
  Stored in directory: /tmp/pip-ephem-wheel-cache-nwscawc7/wheels/29/f3/e0/cc687643d62c9f99247da4aafe149b0bb0de9dc0371bffd5d8
  Building wheel for workerpool (setup.py): started
  Building wheel for workerpool (setup.py): finished with status 'done'
  Created wheel for workerpool: filename=workerpool-0.9.4-py3-none-any.whl size=6378 sha256=f341b244bc75fc4abf4f148894790536bb2ee91a8892c0dda419942ae7229efa
  Stored in directory: /tmp/pip-ephem-wheel-cache-nwscawc7/wheels/8e/87/26/3d6b7c91b3acdc03fb5103f145f4ff24e606bd3a1b3630a9d7
  Building wheel for psutil (pyproject.toml): started
  Building wheel for psutil (pyproject.toml): finished with status 'done'
  Created wheel for psutil: filename=psutil-5.9.1-cp310-cp310-linux_aarch64.whl size=282241 sha256=7dd4d24d648ccb7235ad0fb7119a129a8ca21c4123651c09c06fe7cf85473b5f
  Stored in directory: /tmp/pip-ephem-wheel-cache-nwscawc7/wheels/4f/4f/0f/1cb5a8ab74b6f9128b9cb2025eb1d7ea3c2d5854a55af27e5b
  Building wheel for PyDispatcher (setup.py): started
  Building wheel for PyDispatcher (setup.py): finished with status 'done'
  Created wheel for PyDispatcher: filename=PyDispatcher-2.0.5-py3-none-any.whl size=11516 sha256=4aba4e6b2c1d6b153a4295871eb58a1b0cc1b14a06271e1e0e569528a13009c3
  Stored in directory: /tmp/pip-ephem-wheel-cache-nwscawc7/wheels/14/7c/5c/ee76aa1c988e0bb36e95664fccd4e9270744375d3df26be5fc
Successfully built pypi-xmlrpc workerpool psutil PyDispatcher
Installing collected packages: ssdp, PyDispatcher, pyasn1, jsonrpclib-pelix, xmltodict, workerpool, tzdata, pycparser, psutil, more-itertools, mako, jaraco.context, idna, humanfriendly, formencode, colorama, click, cherrypy, charset-normalizer, certifi, sqlobject, requests, pytz-deprecation-shim, pySMART, jaraco.functools, jaraco.classes, cffi, tzlocal, requests-futures, pynacl, jaraco.text, cryptography, bcrypt, pyopenssl, paramiko, jaraco.collections, apscheduler, pypi-xmlrpc
Successfully installed PyDispatcher-2.0.5 apscheduler-3.9.1 bcrypt-3.2.2 certifi-2022.6.15 cffi-1.15.1 charset-normalizer-2.1.0 cherrypy-8.9.1 click-8.1.3 colorama-0.4.5 cryptography-37.0.4 formencode-2.0.1 humanfriendly-10.0 idna-3.3 jaraco.classes-3.2.1 jaraco.collections-3.5.1 jaraco.context-4.1.1 jaraco.functools-3.5.0 jaraco.text-3.8.0 jsonrpclib-pelix-0.4.3.2 mako-1.2.1 more-itertools-8.13.0 paramiko-2.11.0 psutil-5.9.1 pySMART-1.1.0 pyasn1-0.4.8 pycparser-2.21 pynacl-1.5.0 pyopenssl-22.0.0 pypi-xmlrpc-2020.12.3 pytz-deprecation-shim-0.1.0.post0 requests-2.28.1 requests-futures-1.0.0 sqlobject-3.9.1 ssdp-1.1.0 tzdata-2022.1 tzlocal-4.2 workerpool-0.9.4 xmltodict-0.13.0
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv
[  OK  ] DietPi-Software | pip3 install --no-cache-dir -Ur requirements.txt

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Docker: Build, ship, and run distributed applications

[  OK  ] DietPi-Software | Checking URL: https://download.docker.com/linux/debian/gpg
[  OK  ] DietPi-Software | eval curl -sSfL 'https://download.docker.com/linux/debian/gpg' | gpg --dearmor -o /etc/apt/trusted.gpg.d/dietpi-docker.gpg --yes
[  OK  ] DietPi-Software | eval echo 'deb https://download.docker.com/linux/debian/ bullseye stable' > /etc/apt/sources.list.d/docker.list
[ INFO ] DietPi-Software | APT update, please wait...
Get:1 https://download.docker.com/linux/debian bullseye InRelease [43.3 kB]
Hit:2 https://downloads.plex.tv/repo/deb public InRelease
Hit:3 https://download.mono-project.com/repo/debian buster InRelease
Hit:4 https://deb.debian.org/debian bookworm InRelease
Hit:5 https://packages.grafana.com/oss/deb stable InRelease
Hit:6 https://deb.debian.org/debian bookworm-updates InRelease
Hit:7 https://deb.debian.org/debian-security bookworm-security InRelease
Get:8 https://download.docker.com/linux/debian bullseye/stable arm64 Packages [10.6 kB]
Hit:9 https://download.zerotier.com/debian/bookworm bookworm InRelease
Hit:10 https://deb.debian.org/debian bookworm-backports InRelease
Hit:11 https://archive.raspberrypi.org/debian bullseye InRelease
Hit:12 https://apt.sonarr.tv/debian buster InRelease
Fetched 54.0 kB in 4s (12.4 kB/s)
Reading package lists...
W: https://apt.sonarr.tv/debian/dists/buster/InRelease: Key is stored in legacy trusted.gpg keyring (/etc/apt/trusted.gpg), see the DEPRECATION section in apt-key(8) for details.
[  OK  ] DietPi-Software | APT update
[ INFO ] DietPi-Software | APT install for: docker-ce, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
The following additional packages will be installed:
  containerd.io docker-ce-cli iptables libip6tc2 libnetfilter-conntrack3
  libnfnetlink0 libnftnl11
Suggested packages:
  cgroupfs-mount | cgroup-lite firewalld
Recommended packages:
  apparmor docker-ce-rootless-extras libltdl7 pigz xz-utils nftables
The following NEW packages will be installed:
  containerd.io docker-ce docker-ce-cli iptables libip6tc2
  libnetfilter-conntrack3 libnfnetlink0 libnftnl11
0 upgraded, 8 newly installed, 0 to remove and 0 not upgraded.
Need to get 70.9 MB of archives.
After this operation, 342 MB of additional disk space will be used.
Get:1 https://deb.debian.org/debian bookworm/main arm64 libip6tc2 arm64 1.8.8-1 [34.5 kB]
Get:2 https://deb.debian.org/debian bookworm/main arm64 libnfnetlink0 arm64 1.0.2-2 [14.5 kB]
Get:3 https://deb.debian.org/debian bookworm/main arm64 libnetfilter-conntrack3 arm64 1.0.9-2 [39.5 kB]
Get:4 https://download.docker.com/linux/debian bullseye/stable arm64 containerd.io arm64 1.6.6-1 [20.8 MB]
Get:5 https://deb.debian.org/debian bookworm/main arm64 libnftnl11 arm64 1.2.2-1 [59.8 kB]
Get:6 https://deb.debian.org/debian bookworm/main arm64 iptables arm64 1.8.8-1 [364 kB]
Get:7 https://download.docker.com/linux/debian bullseye/stable arm64 docker-ce-cli arm64 5:20.10.17~3-0~debian-bullseye [36.1 MB]
Get:8 https://download.docker.com/linux/debian bullseye/stable arm64 docker-ce arm64 5:20.10.17~3-0~debian-bullseye [13.4 MB]
debconf: delaying package configuration, since apt-utils is not installed
Fetched 70.9 MB in 17s (4070 kB/s)
                                  Selecting previously unselected package containerd.io.
(Reading database ... 53423 files and directories currently installed.)
Preparing to unpack .../0-containerd.io_1.6.6-1_arm64.deb ...
Unpacking containerd.io (1.6.6-1) ...
Selecting previously unselected package docker-ce-cli.
Preparing to unpack .../1-docker-ce-cli_5%3a20.10.17~3-0~debian-bullseye_arm64.deb ...
Unpacking docker-ce-cli (5:20.10.17~3-0~debian-bullseye) ...
Selecting previously unselected package libip6tc2:arm64.
Preparing to unpack .../2-libip6tc2_1.8.8-1_arm64.deb ...
Unpacking libip6tc2:arm64 (1.8.8-1) ...
Selecting previously unselected package libnfnetlink0:arm64.
Preparing to unpack .../3-libnfnetlink0_1.0.2-2_arm64.deb ...
Unpacking libnfnetlink0:arm64 (1.0.2-2) ...
Selecting previously unselected package libnetfilter-conntrack3:arm64.
Preparing to unpack .../4-libnetfilter-conntrack3_1.0.9-2_arm64.deb ...
Unpacking libnetfilter-conntrack3:arm64 (1.0.9-2) ...
Selecting previously unselected package libnftnl11:arm64.
Preparing to unpack .../5-libnftnl11_1.2.2-1_arm64.deb ...
Unpacking libnftnl11:arm64 (1.2.2-1) ...
Selecting previously unselected package iptables.
Preparing to unpack .../6-iptables_1.8.8-1_arm64.deb ...
Unpacking iptables (1.8.8-1) ...
Selecting previously unselected package docker-ce.
Preparing to unpack .../7-docker-ce_5%3a20.10.17~3-0~debian-bullseye_arm64.deb ...
Unpacking docker-ce (5:20.10.17~3-0~debian-bullseye) ...
Setting up libip6tc2:arm64 (1.8.8-1) ...
Setting up libnftnl11:arm64 (1.2.2-1) ...
Setting up containerd.io (1.6.6-1) ...
Created symlink /etc/systemd/system/multi-user.target.wants/containerd.service → /lib/systemd/system/containerd.service.
Setting up docker-ce-cli (5:20.10.17~3-0~debian-bullseye) ...
Setting up libnfnetlink0:arm64 (1.0.2-2) ...
Setting up libnetfilter-conntrack3:arm64 (1.0.9-2) ...
Setting up iptables (1.8.8-1) ...
update-alternatives: using /usr/sbin/iptables-legacy to provide /usr/sbin/iptables (iptables) in auto mode
update-alternatives: using /usr/sbin/ip6tables-legacy to provide /usr/sbin/ip6tables (ip6tables) in auto mode
update-alternatives: using /usr/sbin/iptables-nft to provide /usr/sbin/iptables (iptables) in auto mode
update-alternatives: using /usr/sbin/ip6tables-nft to provide /usr/sbin/ip6tables (ip6tables) in auto mode
update-alternatives: using /usr/sbin/arptables-nft to provide /usr/sbin/arptables (arptables) in auto mode
update-alternatives: using /usr/sbin/ebtables-nft to provide /usr/sbin/ebtables (ebtables) in auto mode
Setting up docker-ce (5:20.10.17~3-0~debian-bullseye) ...
Created symlink /etc/systemd/system/multi-user.target.wants/docker.service → /lib/systemd/system/docker.service.
Created symlink /etc/systemd/system/sockets.target.wants/docker.socket → /lib/systemd/system/docker.socket.
Processing triggers for libc-bin (2.33-7) ...
[  OK  ] DietPi-Software | APT install for: docker-ce
[  OK  ] DietPi-Software | systemctl stop docker
[  OK  ] DietPi-Software | mkdir /lib/systemd/system/docker.service.d
[  OK  ] DietPi-Software | eval echo -e '[Service]\nType=simple' > /lib/systemd/system/docker.service.d/dietpi-simple.conf
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/docker-data
[  OK  ] DietPi-Software | Comment in /etc/containerd/config.toml converted to setting: [debug]
[  OK  ] DietPi-Software | Comment in /etc/containerd/config.toml converted to setting:   level = "warn"
grep: Unmatched [, [^, [:, [., or [=
[  OK  ] DietPi-Software | sed -i /root=/s/[[:blank:]]*$/ cgroup_enable=memory/ /boot/cmdline.txt

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Docker Compose: Manage multi-container Docker applications

[ INFO ] DietPi-Software | pip3 uninstall -y docker-compose, please wait...
WARNING: Skipping docker-compose as it is not installed.
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv
[  OK  ] DietPi-Software | pip3 uninstall -y docker-compose
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | curl -sSfL https://github.com/docker/compose/releases/download/v2.6.1/docker-compose-linux-aarch64 -o docker-compose-linux-aarch64
[  OK  ] DietPi-Software | mv docker-compose-linux-aarch64 /usr/local/bin/docker-compose
[  OK  ] DietPi-Software | chmod +x /usr/local/bin/docker-compose

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Home Assistant: Open source home automation platform

[ INFO ] DietPi-Software | Home Assistant user:  homeassistant
[ INFO ] DietPi-Software | Home Assistant home:  /home/homeassistant
[ INFO ] DietPi-Software | pyenv activation:     ". /home/homeassistant/pyenv-activate.sh"
[ INFO ] DietPi-Software | pyenv Python version: 3.9.10
[  OK  ] DietPi-Software | Verifying user "homeassistant" to run Home Assistant
[  OK  ] DietPi-Software | useradd -rMU -G dialout,gpio,i2c -d /home/homeassistant -s /usr/sbin/nologin homeassistant
[  OK  ] DietPi-Software | mkdir -p /home/homeassistant
[  OK  ] DietPi-Software | chown homeassistant:homeassistant /home/homeassistant
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://github.com/pyenv/pyenv/archive/master.tar.gz
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://github.com/pyenv/pyenv/archive/master.tar.gz -o master.tar.gz
[ INFO ] DietPi-Software | APT install for: gcc libc6-dev make libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev libffi-dev, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
gcc is already the newest version (4:11.2.0-2).
libc6-dev is already the newest version (2.33-7).
libc6-dev set to manually installed.
libffi-dev is already the newest version (3.4.2-4).
make is already the newest version (4.3-4.1).
libssl-dev is already the newest version (3.0.4-2).
zlib1g-dev is already the newest version (1:1.2.11.dfsg-4).
The following additional packages will be installed:
  libncurses-dev
Suggested packages:
  ncurses-doc readline-doc sqlite3-doc
Recommended packages:
  bzip2-doc
The following NEW packages will be installed:
  libbz2-dev libncurses-dev libreadline-dev libsqlite3-dev
0 upgraded, 4 newly installed, 0 to remove and 0 not upgraded.
Need to get 1494 kB of archives.
After this operation, 6557 kB of additional disk space will be used.
Get:1 https://deb.debian.org/debian bookworm/main arm64 libbz2-dev arm64 1.0.8-5 [30.6 kB]
Get:2 https://deb.debian.org/debian bookworm/main arm64 libncurses-dev arm64 6.3+20220423-2 [335 kB]
Get:3 https://deb.debian.org/debian bookworm/main arm64 libreadline-dev arm64 8.1.2-1.2 [151 kB]
Get:4 https://deb.debian.org/debian bookworm/main arm64 libsqlite3-dev arm64 3.39.0-1 [977 kB]
debconf: delaying package configuration, since apt-utils is not installed
Fetched 1494 kB in 2s (674 kB/s)
                                Selecting previously unselected package libbz2-dev:arm64.
(Reading database ... 53872 files and directories currently installed.)
Preparing to unpack .../libbz2-dev_1.0.8-5_arm64.deb ...
Unpacking libbz2-dev:arm64 (1.0.8-5) ...
Selecting previously unselected package libncurses-dev:arm64.
Preparing to unpack .../libncurses-dev_6.3+20220423-2_arm64.deb ...
Unpacking libncurses-dev:arm64 (6.3+20220423-2) ...
Selecting previously unselected package libreadline-dev:arm64.
Preparing to unpack .../libreadline-dev_8.1.2-1.2_arm64.deb ...
Unpacking libreadline-dev:arm64 (8.1.2-1.2) ...
Selecting previously unselected package libsqlite3-dev:arm64.
Preparing to unpack .../libsqlite3-dev_3.39.0-1_arm64.deb ...
Unpacking libsqlite3-dev:arm64 (3.39.0-1) ...
Setting up libncurses-dev:arm64 (6.3+20220423-2) ...
Setting up libreadline-dev:arm64 (8.1.2-1.2) ...
Setting up libsqlite3-dev:arm64 (3.39.0-1) ...
Setting up libbz2-dev:arm64 (1.0.8-5) ...
[  OK  ] DietPi-Software | APT install for: gcc libc6-dev make libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev libffi-dev
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[  OK  ] DietPi-Software | tar xf master.tar.gz
[  OK  ] DietPi-Software | rm master.tar.gz
[  OK  ] DietPi-Software | mv pyenv-master /home/homeassistant/.pyenv
[  OK  ] DietPi-Software | chown -R homeassistant:homeassistant /home/homeassistant/.pyenv
[ INFO ] DietPi-Software | Installing Python with Home Assistant module into pyenv, please wait...
Downloading Python-3.9.10.tar.gz...
-> https://www.python.org/ftp/python/3.9.10/Python-3.9.10.tgz
Installing Python-3.9.10...
WARNING: The Python lzma extension was not compiled. Missing the lzma lib?
Installed Python-3.9.10 to /home/homeassistant/.pyenv/versions/3.9.10

Requirement already satisfied: pip in ./.pyenv/versions/3.9.10/lib/python3.9/site-packages (21.2.4)
Collecting pip
  Downloading pip-22.1.2-py3-none-any.whl (2.1 MB)
Requirement already satisfied: setuptools in ./.pyenv/versions/3.9.10/lib/python3.9/site-packages (58.1.0)
Collecting setuptools
  Downloading setuptools-63.1.0-py3-none-any.whl (1.2 MB)
Collecting wheel
  Downloading wheel-0.37.1-py2.py3-none-any.whl (35 kB)
Installing collected packages: wheel, setuptools, pip
  Attempting uninstall: setuptools
    Found existing installation: setuptools 58.1.0
    Uninstalling setuptools-58.1.0:
      Successfully uninstalled setuptools-58.1.0
  Attempting uninstall: pip
    Found existing installation: pip 21.2.4
    Uninstalling pip-21.2.4:
      Successfully uninstalled pip-21.2.4
Successfully installed pip-22.1.2 setuptools-63.1.0 wheel-0.37.1
Collecting homeassistant
  Downloading homeassistant-2022.7.3-py3-none-any.whl (18.2 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 18.2/18.2 MB 5.5 MB/s eta 0:00:00
Collecting voluptuous-serialize==2.5.0
  Downloading voluptuous_serialize-2.5.0-py3-none-any.whl (6.8 kB)
Collecting requests==2.28.1
  Downloading requests-2.28.1-py3-none-any.whl (62 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 62.8/62.8 kB 8.9 MB/s eta 0:00:00
Collecting astral==2.2
  Downloading astral-2.2-py2.py3-none-any.whl (30 kB)
Collecting atomicwrites-homeassistant==1.4.1
  Downloading atomicwrites_homeassistant-1.4.1-py2.py3-none-any.whl (7.1 kB)
Collecting PyJWT==2.4.0
  Downloading PyJWT-2.4.0-py3-none-any.whl (18 kB)
Requirement already satisfied: pip<22.2,>=21.0 in ./.pyenv/versions/3.9.10/lib/python3.9/site-packages (from homeassistant) (22.1.2)
Collecting ifaddr==0.1.7
  Downloading ifaddr-0.1.7-py2.py3-none-any.whl (10 kB)
Collecting certifi>=2021.5.30
  Downloading certifi-2022.6.15-py3-none-any.whl (160 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 160.2/160.2 kB 3.6 MB/s eta 0:00:00
Collecting async-timeout==4.0.2
  Downloading async_timeout-4.0.2-py3-none-any.whl (5.8 kB)
Collecting orjson==3.7.5
  Downloading orjson-3.7.5-cp39-cp39-manylinux_2_28_aarch64.whl (249 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 249.7/249.7 kB 3.9 MB/s eta 0:00:00
Collecting python-slugify==4.0.1
  Downloading python-slugify-4.0.1.tar.gz (11 kB)
  Preparing metadata (setup.py): started
  Preparing metadata (setup.py): finished with status 'done'
Collecting yarl==1.7.2
  Downloading yarl-1.7.2-cp39-cp39-manylinux_2_17_aarch64.manylinux2014_aarch64.whl (321 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 321.1/321.1 kB 8.5 MB/s eta 0:00:00
Collecting httpx==0.23.0
  Downloading httpx-0.23.0-py3-none-any.whl (84 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 84.8/84.8 kB 882.8 kB/s eta 0:00:00
Collecting aiohttp==3.8.1
  Downloading aiohttp-3.8.1-cp39-cp39-manylinux_2_17_aarch64.manylinux2014_aarch64.whl (1.2 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.2/1.2 MB 5.3 MB/s eta 0:00:00
Collecting typing-extensions<5.0,>=3.10.0.2
  Downloading typing_extensions-4.3.0-py3-none-any.whl (25 kB)
Collecting bcrypt==3.1.7
  Downloading bcrypt-3.1.7-cp35-abi3-manylinux2014_aarch64.whl (56 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 56.9/56.9 kB 23.2 MB/s eta 0:00:00
Collecting voluptuous==0.13.1
  Downloading voluptuous-0.13.1-py3-none-any.whl (29 kB)
Collecting ciso8601==2.2.0
  Downloading ciso8601-2.2.0.tar.gz (18 kB)
  Installing build dependencies: started
  Installing build dependencies: finished with status 'done'
  Getting requirements to build wheel: started
  Getting requirements to build wheel: finished with status 'done'
  Preparing metadata (pyproject.toml): started
  Preparing metadata (pyproject.toml): finished with status 'done'
Collecting awesomeversion==22.6.0
  Downloading awesomeversion-22.6.0-py3-none-any.whl (11 kB)
Collecting jinja2==3.1.2
  Downloading Jinja2-3.1.2-py3-none-any.whl (133 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 133.1/133.1 kB 6.1 MB/s eta 0:00:00
Collecting cryptography==36.0.2
  Downloading cryptography-36.0.2-cp36-abi3-manylinux_2_17_aarch64.manylinux2014_aarch64.manylinux_2_24_aarch64.whl (3.3 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.3/3.3 MB 6.6 MB/s eta 0:00:00
Collecting attrs==21.2.0
  Downloading attrs-21.2.0-py2.py3-none-any.whl (53 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 53.7/53.7 kB 22.2 MB/s eta 0:00:00
Collecting pyyaml==6.0
  Downloading PyYAML-6.0-cp39-cp39-manylinux_2_17_aarch64.manylinux2014_aarch64.whl (731 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 731.1/731.1 kB 2.2 MB/s eta 0:00:00
Collecting multidict<7.0,>=4.5
  Downloading multidict-6.0.2-cp39-cp39-manylinux_2_17_aarch64.manylinux2014_aarch64.whl (116 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 116.3/116.3 kB 2.5 MB/s eta 0:00:00
Collecting aiosignal>=1.1.2
  Downloading aiosignal-1.2.0-py3-none-any.whl (8.2 kB)
Collecting charset-normalizer<3.0,>=2.0
  Downloading charset_normalizer-2.1.0-py3-none-any.whl (39 kB)
Collecting frozenlist>=1.1.1
  Downloading frozenlist-1.3.0-cp39-cp39-manylinux_2_17_aarch64.manylinux2014_aarch64.whl (156 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 156.8/156.8 kB 7.1 MB/s eta 0:00:00
Collecting pytz
  Downloading pytz-2022.1-py2.py3-none-any.whl (503 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 503.5/503.5 kB 5.7 MB/s eta 0:00:00
Collecting six>=1.4.1
  Downloading six-1.16.0-py2.py3-none-any.whl (11 kB)
Collecting cffi>=1.1
  Downloading cffi-1.15.1-cp39-cp39-manylinux_2_17_aarch64.manylinux2014_aarch64.whl (448 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 448.8/448.8 kB 9.3 MB/s eta 0:00:00
Collecting httpcore<0.16.0,>=0.15.0
  Downloading httpcore-0.15.0-py3-none-any.whl (68 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 68.4/68.4 kB 19.4 MB/s eta 0:00:00
Collecting rfc3986[idna2008]<2,>=1.3
  Downloading rfc3986-1.5.0-py2.py3-none-any.whl (31 kB)
Collecting sniffio
  Downloading sniffio-1.2.0-py3-none-any.whl (10 kB)
Collecting MarkupSafe>=2.0
  Downloading MarkupSafe-2.1.1-cp39-cp39-manylinux_2_17_aarch64.manylinux2014_aarch64.whl (26 kB)
Collecting text-unidecode>=1.3
  Downloading text_unidecode-1.3-py2.py3-none-any.whl (78 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 78.2/78.2 kB 8.1 MB/s eta 0:00:00
Collecting urllib3<1.27,>=1.21.1
  Downloading urllib3-1.26.10-py2.py3-none-any.whl (139 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 139.2/139.2 kB 9.8 MB/s eta 0:00:00
Collecting idna<4,>=2.5
  Downloading idna-3.3-py3-none-any.whl (61 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 61.2/61.2 kB 5.8 MB/s eta 0:00:00
Collecting pycparser
  Downloading pycparser-2.21-py2.py3-none-any.whl (118 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 118.7/118.7 kB 9.8 MB/s eta 0:00:00
Collecting anyio==3.*
  Downloading anyio-3.6.1-py3-none-any.whl (80 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 80.6/80.6 kB 11.8 MB/s eta 0:00:00
Collecting h11<0.13,>=0.11
  Downloading h11-0.12.0-py3-none-any.whl (54 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 54.9/54.9 kB 19.9 MB/s eta 0:00:00
Building wheels for collected packages: ciso8601, python-slugify
  Building wheel for ciso8601 (pyproject.toml): started
  Building wheel for ciso8601 (pyproject.toml): finished with status 'done'
  Created wheel for ciso8601: filename=ciso8601-2.2.0-cp39-cp39-linux_aarch64.whl size=29921 sha256=5c1d35df81cc4bcebf5c31cd64a869d70a6fa3f8f476ed704f003d952a10db9e
  Stored in directory: /tmp/pip-ephem-wheel-cache-0as3ymnt/wheels/eb/ef/30/b91c5119b2581a9d66d18f827d53432f85417ffab180f3e5b8
  Building wheel for python-slugify (setup.py): started
  Building wheel for python-slugify (setup.py): finished with status 'done'
  Created wheel for python-slugify: filename=python_slugify-4.0.1-py2.py3-none-any.whl size=6766 sha256=dfb6bb8dcd3aec703ec573ff089d2d8fcd0f6b681890956aedafbd65c03a4998
  Stored in directory: /tmp/pip-ephem-wheel-cache-0as3ymnt/wheels/84/5b/00/3ebff44b1e0a380d959960828803a9486ff2433728cceff666
Successfully built ciso8601 python-slugify
Installing collected packages: voluptuous, text-unidecode, rfc3986, pytz, ifaddr, ciso8601, voluptuous-serialize, urllib3, typing-extensions, sniffio, six, pyyaml, python-slugify, PyJWT, pycparser, orjson, multidict, MarkupSafe, idna, h11, frozenlist, charset-normalizer, certifi, awesomeversion, attrs, atomicwrites-homeassistant, async-timeout, astral, yarl, requests, jinja2, cffi, anyio, aiosignal, httpcore, cryptography, bcrypt, aiohttp, httpx, homeassistant
Successfully installed MarkupSafe-2.1.1 PyJWT-2.4.0 aiohttp-3.8.1 aiosignal-1.2.0 anyio-3.6.1 astral-2.2 async-timeout-4.0.2 atomicwrites-homeassistant-1.4.1 attrs-21.2.0 awesomeversion-22.6.0 bcrypt-3.1.7 certifi-2022.6.15 cffi-1.15.1 charset-normalizer-2.1.0 ciso8601-2.2.0 cryptography-36.0.2 frozenlist-1.3.0 h11-0.12.0 homeassistant-2022.7.3 httpcore-0.15.0 httpx-0.23.0 idna-3.3 ifaddr-0.1.7 jinja2-3.1.2 multidict-6.0.2 orjson-3.7.5 pycparser-2.21 python-slugify-4.0.1 pytz-2022.1 pyyaml-6.0 requests-2.28.1 rfc3986-1.5.0 six-1.16.0 sniffio-1.2.0 text-unidecode-1.3 typing-extensions-4.3.0 urllib3-1.26.10 voluptuous-0.13.1 voluptuous-serialize-2.5.0 yarl-1.7.2
[  OK  ] DietPi-Software | Installing Python with Home Assistant module into pyenv
[  OK  ] DietPi-Software | chmod +x /home/homeassistant/homeassistant-start.sh
[  OK  ] DietPi-Software | chmod +x /home/homeassistant/homeassistant-update.sh
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/homeassistant
[  OK  ] DietPi-Software | rm -Rf /home/homeassistant/.homeassistant
[  OK  ] DietPi-Software | ln -s /mnt/dietpi_userdata/homeassistant /home/homeassistant/.homeassistant
[  OK  ] DietPi-Software | chown -R homeassistant:homeassistant /mnt/dietpi_userdata/homeassistant

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Domoticz: Open source home automation platform

[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | Checking URL: https://releases.domoticz.com/releases/release/domoticz_linux_aarch64.tgz
[ INFO ] DietPi-Software | G_THREAD_START_0 | curl -sSfL https://releases.domoticz.com/releases/release/domoticz_linux_aarch64.tgz -o domoticz_linux_aarch64.tgz
[ INFO ] DietPi-Software | APT install for: libusb-0.1 libcurl3-gnutls, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
libcurl3-gnutls is already the newest version (7.83.1-2).
libcurl3-gnutls set to manually installed.
The following NEW packages will be installed:
  libusb-0.1-4
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 21.5 kB of archives.
After this operation, 59.4 kB of additional disk space will be used.
Get:1 https://deb.debian.org/debian bookworm/main arm64 libusb-0.1-4 arm64 2:0.1.12-32 [21.5 kB]
debconf: delaying package configuration, since apt-utils is not installed
Fetched 21.5 kB in 0s (47.7 kB/s)
                                 Selecting previously unselected package libusb-0.1-4:arm64.
(Reading database ... 53990 files and directories currently installed.)
Preparing to unpack .../libusb-0.1-4_2%3a0.1.12-32_arm64.deb ...
Unpacking libusb-0.1-4:arm64 (2:0.1.12-32) ...
Setting up libusb-0.1-4:arm64 (2:0.1.12-32) ...
Processing triggers for libc-bin (2.33-7) ...
[  OK  ] DietPi-Software | APT install for: libusb-0.1 libcurl3-gnutls
[  OK  ] DietPi-Software | G_THREAD: All threads finished
[  OK  ] DietPi-Software | tar xf domoticz_linux_aarch64.tgz --one-top-level=/opt/domoticz
[  OK  ] DietPi-Software | rm domoticz_linux_aarch64.tgz
[  OK  ] DietPi-Software | mkdir /mnt/dietpi_userdata/domoticz
[  OK  ] DietPi-Software | cp /opt/domoticz/scripts/domoticz.conf /mnt/dietpi_userdata/domoticz/domoticz.conf
[  OK  ] DietPi-Software | Comment in /mnt/dietpi_userdata/domoticz/domoticz.conf converted to setting: http_port=8124
[  OK  ] DietPi-Software | Comment in /mnt/dietpi_userdata/domoticz/domoticz.conf converted to setting: ssl_port=8424
[  OK  ] DietPi-Software | Comment in /mnt/dietpi_userdata/domoticz/domoticz.conf converted to setting: ssl_cert=/opt/domoticz/server_cert.pem
[  OK  ] DietPi-Software | Comment in /mnt/dietpi_userdata/domoticz/domoticz.conf converted to setting: ssl_key=/opt/domoticz/server_cert.pem
[  OK  ] DietPi-Software | Comment in /mnt/dietpi_userdata/domoticz/domoticz.conf converted to setting: ssl_dhparam=/opt/domoticz/server_cert.pem
[  OK  ] DietPi-Software | Comment in /mnt/dietpi_userdata/domoticz/domoticz.conf converted to setting: loglevel=error
[  OK  ] DietPi-Software | Comment in /mnt/dietpi_userdata/domoticz/domoticz.conf converted to setting: syslog=local7
[  OK  ] DietPi-Software | Comment in /mnt/dietpi_userdata/domoticz/domoticz.conf converted to setting: dbase_file=/mnt/dietpi_userdata/domoticz/domoticz.db
[  OK  ] DietPi-Software | Comment in /mnt/dietpi_userdata/domoticz/domoticz.conf converted to setting: app_path=/opt/domoticz
[  OK  ] DietPi-Software | Comment in /mnt/dietpi_userdata/domoticz/domoticz.conf converted to setting: userdata_path=/mnt/dietpi_userdata/domoticz
[  OK  ] DietPi-Software | Verifying user "domoticz" to run Domoticz
[  OK  ] DietPi-Software | useradd -rMU -G dialout -d /mnt/dietpi_userdata/domoticz -s /usr/sbin/nologin domoticz
[  OK  ] DietPi-Software | chown -R domoticz:domoticz /opt/domoticz /mnt/dietpi_userdata/domoticz
[  OK  ] DietPi-Software | cp -a /opt/domoticz/scripts /mnt/dietpi_userdata/domoticz/

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Portainer: Simplifies container management in Docker (standalone host)

[  OK  ] DietPi-Software | docker volume create portainer_data
[ INFO ] DietPi-Software | Portainer will be deployed now. This could take a while...
[ INFO ] DietPi-Software | docker run -d -p 9002:9000 --name=portainer --restart=always -v /run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce, please wait...
Unable to find image 'portainer/portainer-ce:latest' locally
latest: Pulling from portainer/portainer-ce
772227786281: Pulling fs layer
96fd13befc87: Pulling fs layer
53dd436fc5d5: Pulling fs layer
9ff1f79510e7: Pulling fs layer
9ff1f79510e7: Waiting
772227786281: Verifying Checksum
772227786281: Download complete
96fd13befc87: Verifying Checksum
96fd13befc87: Download complete
772227786281: Pull complete
96fd13befc87: Pull complete
9ff1f79510e7: Verifying Checksum
9ff1f79510e7: Download complete
53dd436fc5d5: Verifying Checksum
53dd436fc5d5: Download complete
53dd436fc5d5: Pull complete
9ff1f79510e7: Pull complete
Digest: sha256:b8573c23e98eb3dc3a59644c15d1c1448f5281ac7972faf996fce24b7511fda6
Status: Downloaded newer image for portainer/portainer-ce:latest
0ba947aaedfd657c642ba20957e3a563411c7247eb1130c89c0be48dcb1ee716
[  OK  ] DietPi-Software | docker run -d -p 9002:9000 --name=portainer --restart=always -v /run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Uninstalling DietPi-RAMlog: Makes /var/log a RAM disk, preserves file structure on reboot

[  OK  ] DietPi-Software | sed -i /[[:blank:]]\/var\/log[[:blank:]]/d /etc/fstab
[  OK  ] DietPi-Software | mkdir -p /var/lib/dietpi/dietpi-ramlog
[  OK  ] DietPi-Software | chmod +x /var/lib/dietpi/dietpi-ramlog/disable.sh
[  OK  ] DietPi-Software | systemctl daemon-reload
[  OK  ] DietPi-Software | systemctl enable dietpi-ramlog_disable

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Finalising uninstall

[ INFO ] DietPi-Software | APT autopurge, please wait...
Reading package lists...
Building dependency tree...
Reading state information...
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
[  OK  ] DietPi-Software | APT autopurge
[  OK  ] DietPi-Software | systemctl daemon-reload

 DietPi-Software
─────────────────────────────────────────────────────
 Step: Uninstall completed


 DietPi-Software
─────────────────────────────────────────────────────
 Step: Finalising install

[  OK  ] DietPi-Software | systemctl daemon-reload
[ INFO ] DietPi-Software | Enabling systemd-logind
[  OK  ] DietPi-Software | systemctl unmask dbus
[  OK  ] DietPi-Software | systemctl start dbus
[  OK  ] DietPi-Software | systemctl unmask systemd-logind
[  OK  ] DietPi-Software | systemctl start systemd-logind
2022-07-12 13:53:55 [ INFO ] DietPi-RAMlog | Storing /var/log to /var/tmp/dietpi/logs/dietpi-ramlog_store...
2022-07-12 13:53:55 [  OK  ] DietPi-RAMlog | Stored /var/log to /var/tmp/dietpi/logs/dietpi-ramlog_store.
[ SUB1 ] DietPi-Services > dietpi_controlled 
[  OK  ] DietPi-Services | dietpi_controlled : avahi-daemon
[  OK  ] DietPi-Services | dietpi_controlled : frpc
[  OK  ] DietPi-Services | dietpi_controlled : nmbd
[  OK  ] DietPi-Services | dietpi_controlled : smbd
[  OK  ] DietPi-Services | dietpi_controlled : mariadb
[  OK  ] DietPi-Services | dietpi_controlled : php8.1-fpm
[  OK  ] DietPi-Services | dietpi_controlled : nginx
[  OK  ] DietPi-Services | dietpi_controlled : rtorrent
[  OK  ] DietPi-Services | dietpi_controlled : nzbget
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
[ SUB1 ] DietPi-Set_hardware > headless (disable)
[  OK  ] DietPi-Set_hardware | sed -i /^[[:blank:]]*max_framebuffers=/c\#max_framebuffers=2 /boot/config.txt
[  OK  ] DietPi-Set_hardware | sed -i /^[[:blank:]]*hdmi_ignore_hotplug=/c\#hdmi_ignore_hotplug=0 /boot/config.txt
[  OK  ] DietPi-Set_hardware | sed -i /^[[:blank:]]*enable_tvout=/c\#enable_tvout=0 /boot/config.txt
[  OK  ] DietPi-Set_hardware | Desired setting in /boot/dietpi.txt was already set: AUTO_SETUP_HEADLESS=0
[  OK  ] headless disable | Completed
[  OK  ] DietPi-AutoStart | Desired setting in /boot/dietpi.txt was already set: AUTO_SETUP_AUTOSTART_LOGIN_USER=root
[  OK  ] DietPi-AutoStart | mkdir -p /etc/systemd/system/getty@tty1.service.d /etc/systemd/system/console-getty.service.d
[  OK  ] DietPi-AutoStart | systemctl daemon-reload

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
[  OK  ] DietPi-Services | restart : rtorrent
[  OK  ] DietPi-Services | restart : nzbget
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
[  OK  ] DietPi-Services | restart : domoticz
[  OK  ] DietPi-Services | restart : htpc-manager
[  OK  ] DietPi-Services | restart : docker
[  OK  ] DietPi-Services | restart : cron
[ INFO ] DietPi-Software | Starting installed services, not controlled by DietPi-Services
[  OK  ] DietPi-Software | systemctl enable adguardhome
[  OK  ] DietPi-Software | systemctl start adguardhome
```

---

Link to original note: [| 12 Jul 2022](Tue)
