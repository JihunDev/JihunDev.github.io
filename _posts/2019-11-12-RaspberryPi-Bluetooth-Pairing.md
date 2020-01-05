---
layout: post
title: RaspberryPi bluetooth paring
tags: RaspberryPi
comments: true
---
# Bluetooth Pairing

## 1. Bluez install
```shell
$ sudo apt-get install bluez libbluetooth-dev pi-bluetooth
```
### Python 3.6이상
Python 3.6 이후 버전은 SSL을 요구하기 떄문에 설치
```shell
$ sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev
```

## 2. 시리얼 포트 등록
```shell
$ sudo sdptool SP
```

## 3. Bluetooth 서비스 실행옵션 수정
```shell
$ sudo systemctl daemon-reload
$ sudo vi /lib/systemd/system/bluetooth.service
  #ExecStart=/usr/lib/bluetooth/bluetoothd -C 로 수정
$ sudo systemctl resart Bluetooth
$ sudo systemctl enable Bluetooth
```

## 4. 장치 내 블루투스 Discoverable 상태로 변경
```shell
$ sudo hciconfig hci0 piscan
```