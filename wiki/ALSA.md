---
aliases:
  - ALSA
tags: wiki homeserver services dietpi docs 
created: 2022-07-12T05:32:22-07:00
updated: 2022-07-29T02:47:11-07:00
title: ALSA
date created: Tuesday, July 12th 2022, 5:31:27 am
date modified: Thursday, July 28th 2022, 6:32:38 pm
linter-yaml-title-alias: ALSA
---

# ALSA

```ad-abstract
Advanced Linux Sound Architecture
```

## Install logs

Tue 12-Jul-2022@05:32:22AM

```bash
DietPi-Software
─────────────────────────────────────────────────────
 Step: Installing ALSA: Advanced Linux Sound Architecture

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
```

## Install logs

Wed 13-Jul-2022@08:07:26AM

```cpp
 Step: Installing [[ALSA]]: Advanced Linux Sound Architecture

[ SUB1 ] DietPi-Set_hardware > soundcard (rpi-bcm2835-auto)
[ INFO ] DietPi-Set_hardware | Checking for required APT packages: alsa-utils
[ INFO ] DietPi-Set_hardware | Resetting all sound card settings...
[  OK  ] DietPi-Set_hardware | rm /etc/asound.conf
[  OK  ] DietPi-Set_hardware | rm /var/lib/alsa/asound.state
alsa-lib parser.c:2775:(load_toplevel_config) Unable to find the top-level configuration file '/usr/share/alsa/ucm2/ucm.conf'.
alsa-lib main.c:1541:(snd_use_case_mgr_open) error: failed to import hw:0 use case configuration -2
Found hardware: "vc4-hdmi" "" "" "" ""
Hardware is initialized using a generic method
alsa-lib parser.c:2775:(load_toplevel_config) Unable to find the top-level configuration file '/usr/share/alsa/ucm2/ucm.conf'.
alsa-lib main.c:1541:(snd_use_case_mgr_open) error: failed to import hw:1 use case configuration -2
Found hardware: "vc4-hdmi" "" "" "" ""
Hardware is initialized using a generic method
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
```
---

Link to original note: [[ihomeserver install logs media server services]]
