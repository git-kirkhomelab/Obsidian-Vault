---
aliases:
  - go
tags: 
created: 2022-07-12T08:28:31-07:00
updated: 2022-07-29T02:50:35-07:00
title: go
linter-yaml-title-alias: go
date created: Tuesday, July 12th 2022, 8:27:03 am
date modified: Thursday, July 28th 2022, 6:32:34 pm
---

# go

```ad-abstract
Runtime environment and package installer 
```

# Install logs

```c
 DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing [[Go]]: Runtime environment and package installer

[  OK  ] DietPi-Software | rm -R /usr/local/go
[  OK  ] DietPi-Software | cd /tmp/DietPi-Software
[  OK  ] DietPi-Software | curl -sSfL https://golang.org/dl/go1.18.3.linux-arm64.tar.gz -o go1.18.3.linux-arm64.tar.gz
[  OK  ] DietPi-Software | tar xf go1.18.3.linux-arm64.tar.gz --one-top-level=/usr/local
[  OK  ] DietPi-Software | rm go1.18.3.linux-arm64.tar.gz
[  OK  ] DietPi-Software | mkdir -p /mnt/dietpi_userdata/go/bin /mnt/dietpi_userdata/go/pkg /mnt/dietpi_userdata/go/src
```
