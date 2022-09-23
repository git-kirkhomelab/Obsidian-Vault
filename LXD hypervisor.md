---
aliases:
  - Setup config details
tags: 
created: 2022-07-26T21:52:26-07:00
updated: 2022-07-29T02:47:13-07:00
title: Setup config details
linter-yaml-title-alias: Setup config details
date created: Tuesday, July 26th 2022, 9:51:04 pm
date modified: Thursday, July 28th 2022, 6:33:00 pm
---
```ad-abstract
Ubuntu 22.04 ARM Server 
> [Run Linux Containers with LXC/LXD on Ubuntu 22.04|20.04|18.04 - TechViewLeo](https://techviewleo.com/run-linux-containers-with-lxc-lxd-on-ubuntu/)
> 

```

# Setup config details

```cpp
ubuntu@ubuntu:~$ sudo lxd init                                                                                          Would you like to use LXD clustering? (yes/no) [default=no]:                                                            Do you want to configure a new storage pool? (yes/no) [default=yes]:                                                    Name of the new storage pool [default=default]:                                                                         Name of the storage backend to use (ceph, btrfs, dir, lvm, zfs) [default=zfs]:                                          Create a new ZFS pool? (yes/no) [default=yes]:                                                                          Would you like to use an existing empty block device (e.g. a disk or partition)? (yes/no) [default=no]: yes             Path to the existing block device: /dev/sdb                                                                             Would you like to connect to a MAAS server? (yes/no) [default=no]:                                                      Would you like to create a new local network bridge? (yes/no) [default=yes]:                                            What should the new bridge be called? [default=lxdbr0]:                                                                 What IPv4 address should be used? (CIDR subnet notation, “auto” or “none”) [default=auto]:                              What IPv6 address should be used? (CIDR subnet notation, “auto” or “none”) [default=auto]:                              Would you like the LXD server to be available over the network? (yes/no) [default=no]: yes                              Address to bind LXD to (not including port) [default=all]:                                                              Port to bind LXD to [default=8443]:                                                                                     Trust password for new clients:                                                                                         Again:                                                                                                                  Invalid input, try again.                                                                                                                                                                                                                       Trust password for new clients:   # homelab                                                                                       Again:   # homelab                                                                                                                Would you like stale cached images to be updated automatically? (yes/no) [default=yes]:                                 Would you like a YAML "lxd init" preseed to be printed? (yes/no) [default=no]: yes                                      config:                                                                                                                   core.https_address: '[::]:8443'                                                                                         core.trust_password: homelab                                                                                          networks:                                                                                                               - config:                                                                                                                   ipv4.address: auto                                                                                                      ipv6.address: auto                                                                                                    description: ""                                                                                                         name: lxdbr0                                                                                                            type: ""                                                                                                                project: default                                                                                                      storage_pools:                                                                                                          - config:                                                                                                                   source: /dev/sdb                                                                                                      description: ""                                                                                                         name: default                                                                                                           driver: zfs                                                                                                           profiles:                                                                                                               - config: {}                                                                                                              description: ""                                                                                                         devices:                                                                                                                  eth0:                                                                                                                     name: eth0                                                                                                              network: lxdbr0                                                                                                         type: nic                                                                                                             root:                                                                                                                     path: /                                                                                                                 pool: default                                                                                                           type: disk                                                                                                          name: default                                                                                                         projects: []                                                                                                            cluster: null   
```

Basic steps to produce hypervisor image

```cpp
$ sudo lxd init 
# confirm container is running 
$ sudo lxc info | more 
# launch container <os-version> with <name>
$ sudo lxc launch <os-version, ie, "ubuntu:20.04"> <name, ie, "vas">
# list running containers
$ sudo lxc list 
# to enter the container <"vas"> 
$ sudo lxc exec vas bash 
root@vas:~$ 
# get ip address of running container <"vas">
root@vas:~$ ip a
```

Container management

```cpp
# start|stop|restart <"vas">
$ sudo lxc <start|stop|restart> vas
# verify container status
$ sudo lxc list 
# to delete a container <"vas"> 
$ sudo lxc delete vas 
# to take a snapshot of container <"vas"> with snapshot name <"vas-snap1"> 
$ sudo lxc snapshot vas vas-snap1
# to check snapshot creation status
$ sudo lxc info vas | grep -i Snapshots -A2
# to restore snapshot 
$ sudo lxc restore vas vas-snap1
```

```cardlink
url: https://techviewleo.com/run-linux-containers-with-lxc-lxd-on-ubuntu/
title: "Run Linux Containers with LXC/LXD on Ubuntu 22.04|20.04|18.04 - TechViewLeo"
description: "What is virtualization? Virtualization is the abstraction of a host computing resources such as storage, CPU, RAM and networking to create virtual machines or"
host: techviewleo.com
favicon: https://techviewleo.com/wp-content/uploads/2019/01/android-chrome-192x192.png
image: https://techviewleo.com/wp-content/uploads/2020/09/lxd-containers.png
```

	
