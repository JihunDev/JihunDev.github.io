---
title: BeagleBone Black Wirelsee Wi-Fi 접속
categories:
  - BeagleBone
  
tags: BeagleBone

toc: true
toc_label: "On This Page"
toc_icon: "cog"
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
