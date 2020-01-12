---
layout: post
title: CLI로 Wi-Fi 접속
tags: Linux
comments: true
use_math: true
---

ubuntu Command Line Wi-Fi 접속

```shell
$ nmcli dev wifi list
$ nmcli dev wifi con 'SSID' password 'Wi-Fi Password'
```



## Error: Failed to add/activate new connection: Not authorized to control networking.

```shell
$ sudo nmcli dev wifi con 'SSID' password 'Wi-Fi Password'
```

sudo 붙여주면 인증
