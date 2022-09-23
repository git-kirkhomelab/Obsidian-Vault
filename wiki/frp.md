---
aliases:
  - FRP
tags: 
created: 2022-07-12T05:17:41-07:00
updated: 2022-07-29T02:47:10-07:00
title: FRP
linter-yaml-title-alias: FRP
date created: Tuesday, July 12th 2022, 5:14:06 am
date modified: Thursday, July 28th 2022, 6:32:35 pm
---

# FRP

- frp client on homserver
- frp server on ionos vps

```shell
$ ssh root@74.208.118.170
# password hHNoC258_#
$ wget https://github.com/fatedier/frp/releases/download/v0.33.0/frp_0.33.0_linux_amd64.tar.gz
$ mkdir /home/frp
$ tar -zxvf frp_0.33.0_linux_amd64.tar.gz -C /home/frp/
$ cd /home/frp/frp_0.33.0_linux_amd64/
$ nano frps.ini
#port_check_tool 
# sudo lsof -i:7000 # appears to be available so I'll give it a shot
# .ini file is as follows:
[common]
bind_port = 7000
# start frps on vps
$ ./frps -c ./frps.ini
```

Description of bind_port i:

	bind_port: The bound port, which needs to be consistent with the server_port parameter in the client. vhost_http_port: The port on which the virtual host runs on the machine. If the port is occupied by a vps service, you should replace the dashboard_port: port of the frp background service page. If you set 8000, You can access the background page of frps through http://yourip:8000 dashboard_user: the administrator user name of the frp background service page dashboard_pwd: the administrator password of the frp background service page privilege_token: a custom value, which must be the same as the privilege_token in the client be consistent

source: [Raspberry Pi: Use peanut shell or FRP to achieve intranet penetration and remote access - Knowledge - GNS Components Limited](https://www.ictransistors.com/info/raspberry-pi-use-peanut-shell-or-frp-to-achie-47856815.html)

set auth token to 12345678 at ionos based on:

[frp/frps_full.ini at 6f2571980c2688cbfd5ed0bf2a0cbf753d3352c6 · fatedier/frp · GitHub](https://github.com/fatedier/frp/blob/6f2571980c2688cbfd5ed0bf2a0cbf753d3352c6/conf/frps_full.ini)

```cardlink
url: https://github.com/fatedier/frp/blob/6f2571980c2688cbfd5ed0bf2a0cbf753d3352c6/conf/frps_full.ini
title: "frp/frps_full.ini at 6f2571980c2688cbfd5ed0bf2a0cbf753d3352c6 · fatedier/frp"
description: "A fast reverse proxy to help you expose a local server behind a NAT or firewall to the internet. - frp/frps_full.ini at 6f2571980c2688cbfd5ed0bf2a0cbf753d3352c6 · fatedier/frp"
host: github.com
favicon: https://github.githubassets.com/favicons/favicon.svg
image: https://opengraph.githubassets.com/7779bd60cad737f571347a181bb5ed5466e2fe17a1e116c8ba68a922fd714183/fatedier/frp
```

[port_check_tool](port_check_tool.md)

```shell
$ sudo lsof -i:<port>
```
