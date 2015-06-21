---
layout: post
title: "Ubuntu意外卸载network manager的解决办法"
category: "Ubuntu"
tags: ["Ubuntu","命令行连接wifi"]
--- 

已经很久没有在博客里写任何关于IT的东西了，今天重新开个头
当作备忘录用吧。
折腾ubuntu的时候不小心把network-manager卸载掉了，系统连不了网。
apt-get用不了，下载的deb包但是依赖问题不好解决。
google一下其实可以用cli连接wifi的，命令如下。

    wpa_passphrase ssid password > foo.conf
    killall -9 wpa_supplicant
    sudo wpa_supplicant -Dwext -i wlan0 -c foo.conf

连上之后，dhcp请求一个ip
    dhcpclient wlan0

ok应该可以上了。

---
