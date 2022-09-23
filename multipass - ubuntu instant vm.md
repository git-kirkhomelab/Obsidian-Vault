---
aliases:
  - Install guide
tags: 
created: 2022-07-27T00:32:01-07:00
updated: 2022-07-29T02:50:38-07:00
title: Install guide
linter-yaml-title-alias: Install guide
date created: Wednesday, July 27th 2022, 12:26:58 am
date modified: Thursday, July 28th 2022, 6:32:55 pm
---
```ad-abstract
Multipass can launch and run virtual machines and configure them with [cloud-init](https://cloud-init.io/) like a public cloud. Prototype your cloud launches locally for free.

```

# Install guide

```
# install on linux 
$ sudo snap install multipass 
	# launch an instance (default is current ubuntu LTS)
$ multipass launch --name <VM>
# to run commands in bash shell in that instance 
$ multipass exec <VM> -- lsb_release -a 
# see instances status 
$ multipass list 
# stop and start instances 
$ multipass stop <VM> bar 
$ multipass start <VM> 
# clean up 
$ multipass delete bar 
$ multipass purge  
# alternate images 
$ multipass find 
```

# Authentication

```cpp
$ multipass authenticate 
# if first time, then run 
$ multipass set local.passphrase 
# passphrase set to "homelab"
```
