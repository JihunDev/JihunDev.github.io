---
layout: post
title: Linux Can-utils
tags: Linux CAN
comments: true
---

Linux 환경에서 can-utils를 이용하여 자동차의 CAN 정보 확인

## can-utils Install
```shell
$ apt install can-utils
```

## candump 사용법

```shell
$ candump vcan0
 vcan0  123   [4]  01 AA BB 22
 vcan0  123   [4]  01 AA BB 23
 vcan0  123   [4]  01 AA BB 24
```

## reference
[github:can-utils](https://github.com/linux-can/can-utils)