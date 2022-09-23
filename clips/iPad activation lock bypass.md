---
# Metadata used for sync
id: "b6a54950-f3d2-11ec-abab-e15e7216634b"
title: "iPad activation lock bypass"
created: "2022-06-24T15:31:27.461Z"
source: "https://checkra.in/linux"
---
$ sudo su 
$ wget -O - https://assets.checkra.in/debian/archive.key | gpg --dearmor | sudo tee /usr/share/keyrings/checkra1n.gpg >/dev/null
$ echo 'deb [signed-by=/usr/share/keyrings/checkra1n.gpg] https://assets.checkra.in/debian /' | sudo tee /etc/apt/sources.list.d/checkra1n.list
$ sudo apt-get update
$ sudo apt-get install checkra1n