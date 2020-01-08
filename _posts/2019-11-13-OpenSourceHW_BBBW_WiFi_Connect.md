---
layout: post
title: BeagleBone Black Wirelsee Wi-Fi 접속
tags: BeagleBone
comments: true
---

비글본 블랙 와이파이 접속법

## Command
```shell
$ sudo connmanctl
connmanctl> tether wifi disable
connmanctl> enable wifi
connmanctl> scan wifi
connmanctl> services
connmanctl> agent on
connmanctl> connect <wifi network>
connmanctl> quit
```
