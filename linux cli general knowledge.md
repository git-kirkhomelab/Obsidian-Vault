---
aliases:
  - Networking
tags: 
created: 2022-07-26T22:28:03-07:00
updated: 2022-07-29T04:03:14:19-07:00
title: Networking
linter-yaml-title-alias: Networking
date created: Tuesday, July 26th 2022, 10:26:35 pm
date modified: Thursday, July 28th 2022, 6:32:57 pm
---
## Networking

### Port check tool/port scan

1. netstat
```cpp
# to list all ports in use 
$ sudo netstat -tunlp 
# to check a specific port, then use 
$ sudo netstat -tunlp | grep :<PORT#> # note the space between "grep" and "port"
```

2. ss
```cpp
# to get a list of all ports in use 
$ sudo ss -tunlp 
# this may be faster than netstat 
```

3. lsof
```cpp
# to get a list of all listening ports with process name
$ sudo lsof -nP -iTCP -sTCP:LISTEN 
# to check a specific port and get the process name 
$ sudo lsof -nP -iTCP:<PORT#> -sTCP:LISTEN
```

```cardlink
url: https://blog.fearcat.in/a?ID=01450-c814941c-b046-4ef0-a5b5-a8240df63eea
title: "How to view the port being used in Linux - Fear Cat"
host: blog.fearcat.in
```


## User Management 
```shell
# to add new user 
$ sudo adduser <username>
# to add user to sudo group 
$ sudo usermod -aG sudo <username>
```

```cardlink
url: https://linuxize.com/post/how-to-add-user-to-sudoers-in-ubuntu/
title: "How to Add User to Sudoers in Ubuntu"
description: "On Ubuntu, the easiest way to grant sudo privileges to a user is by adding the user to the sudo group. Members of this group will be able to execute any command as root via sudo."
host: linuxize.com
favicon: /favicons/favicon-32x32.png
image: https://linuxize.com/post/how-to-add-user-to-sudoers-in-ubuntu/featured.jpg
```

