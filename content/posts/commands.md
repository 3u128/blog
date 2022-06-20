---
title: "usefull commands"
date: 2022-05-08
draft: true
---
:se paste noai
https://stackoverflow.com/questions/2514445/turning-off-auto-indent-when-pasting-text-into-vim#:~:text=Go%20to%20Vim%20and%20press,Paste%22%20from%20the%20popup%20menu.

/sys/devices/platform/i8042/serio1/serio2/sensitivity
/sys/devices/platform/i8042/serio1/serio2/speed
source:
https://gist.githubusercontent.com/noromanba/11261595/raw/478cf4c4d9b63f1e59364a6f427ffccd63db5e1e/thinkpad-trackpoint-speed.mkd

For example, to override the pointing speed, create /etc/libinput/local-overrides.quirks:

[Trackpoint Override]
MatchUdevType=pointingstick
AttrTrackpointMultiplier=0.75
source:
https://wiki.archlinux.org/title/TrackPoint#device-quirks
