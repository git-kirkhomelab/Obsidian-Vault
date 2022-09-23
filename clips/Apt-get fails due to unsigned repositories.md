---
# Metadata used for sync
id: "4227d070-f3d2-11ec-b891-23703a4c9058"
title: "Apt-get fails due to unsigned repositories"
created: "2022-06-24T15:28:12.023Z"
source: "https://askubuntu.com/questions/732985/force-update-from-unsigned-repository-="
---
$ apt-get update --allow-insecure-repositories
$ apt-get install <package> --allow-unauthenticated # may not be necessary