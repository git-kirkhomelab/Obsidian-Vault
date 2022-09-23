---
aliases:
  - Python 3
tags: 
created: 2022-07-12T08:23:38-07:00
updated: 2022-07-29T02:47:03-07:00
title: Python 3
linter-yaml-title-alias: Python 3
date created: Tuesday, July 12th 2022, 8:21:47 am
date modified: Thursday, July 28th 2022, 6:32:33 pm
---

# Python 3

```ad-abstract
Runtime system, pip package installer and development headers 
```

# Install logs

```c
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
```
