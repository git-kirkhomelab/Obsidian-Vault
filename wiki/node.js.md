---
aliases:
  - node.js
tags: 
created: 2022-07-12T08:14:02-07:00
updated: 2022-07-29T02:47:08-07:00
title: node.js
date created: Tuesday, July 12th 2022, 8:13:24 am
date modified: Thursday, July 28th 2022, 6:32:33 pm
linter-yaml-title-alias: node.js
---

# node.js

```ad-abstract
JavaScript runtime environment 
```

# Install logs

```c
 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing Node.js: JavaScript runtime environment

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
```
