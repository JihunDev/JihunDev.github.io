---
layout: post
title: Android ADB 이용 SmartPhone 접속
tags: Android ADB
comments: true
---

Android USB선 없이 디버깅

## ADB을 이용해서 무선으로 Android 연결 방법

> PC와 Android Smart Phone이 같은 Wi-Fi상에 존재 해야함
### 설정 방법
1.  Smart Phone과 PC를 USB 연결
2. 터미널에 아래와 같이 설정
```shell
# MacOS or Linux
$ cd /Users/andrew/Library/Android/sdk/platform-tools
$ ./adb tcpip 5555
# Windows
> adb tcpip 5555
```
- 터미널에서 /Users/\<UserName\>/Library/Android/sdk/platform-tools/의 adb파일이 있는 곳에서 실행
- ADB로 사용할 포트 번호 설정(5555)

3. Android와 PC연결
```bash
# MacOS or Linux
$ ./adb connect 5555
# Windows
> adb connect 5555 
```