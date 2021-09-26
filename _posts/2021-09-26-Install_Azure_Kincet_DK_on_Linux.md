---
title: Azure Kincet Sensor DK Ubuntu 설치 방법
author: Jihun Kim
date: 2021-09-26 00:00:00 +0000
categories: [Device, Kincet]
tags: [Kincet]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

# info

- Microsoft's Installation Guide

[microsoft/Azure-Kinect-Sensor-SDK](https://github.com/microsoft/Azure-Kinect-Sensor-SDK/blob/develop/docs/usage.md#debian-package)

[Linux Software Repository for Microsoft Products](https://docs.microsoft.com/en-us/windows-server/administration/linux-package-repository-for-microsoft-software#ubuntu)

# Install Guide

## 1. Add link to Microsft Linux Software Repository

```bash
$ curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
$ sudo apt-add-repository https://packages.microsoft.com/ubuntu/18.04/prod
$ sudo apt-get update
```

### 1. curl 미설치시

```bash
$ sudo apt update && upgrade
$ sudo apt install curl
```

### 2. i386 에러 출력시

- 아래와 같은 Error 출력시 [arch=amd64] 스팩을 추가

```bash
$ sudo apt-get update: N: Skipping acquire of configured file 'main/binary-i386/Packages' as repository 'https://packages.microsoft.com/ubuntu/18.04/prod' doesn't support support architecture 'i386'
```

- /etc/apt/sources.list 수정

```bash
deb https://packages.microsoft.com/ubuntu/18.04/prod bionic main
# deb-src https://packages.microsoft.com/ubuntu/18.04/prod bionic main
```

to:

```bash
deb [arch=amd64] https://packages.microsoft.com/ubuntu/18.04/prod bionic main
# deb-src [arch=amd64] https://packages.microsoft.com/ubuntu/18.04/prod bionic main
```

## 2. Install Kincet Package

- Repository Error가 없을시 실행

> libk4a1.x와 lib4a1.x-dev의 version은 같아야 함

```bash
$ sudo apt-get update
```

```bash
$ sudo apt install k4a-tools
$ sudo apt install libk4a1.4 libk4a1.4-dev
```

잘못설치 시 $ sudo apt remove k4a-tools

## 3. Device Setup

- Microsoft's  udev Setting Guide

[microsoft/Azure-Kinect-Sensor-SDK](https://github.com/microsoft/Azure-Kinect-Sensor-SDK/blob/develop/docs/usage.md#linux-device-setup)

- udev 규칙 설정
    - Github에 file Clone
    - 복사 후 Azure Kinect 분리 후 다시 연결

```bash
$ git clone https://github.com/microsoft/Azure-Kinect-Sensor-SDK/blob/develop/scripts/99-k4a.rules
$ sudo cp scripts/99-k4a.rules /etc/udev/rules.d/
```

## 4. Run to APP

```bash
$ k4aviewer
```