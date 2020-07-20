---
layout: post
title: ubuntu NodeJs 설치
tags: nodejs ubuntu
comments: true
---

ubuntu nodejs 설치 방법

## nodejs version 10
```shell
$ sudo apt-get update
$ sudo apt-get install -y bulid-essential
$ sudo apt-get install curl
```

```shell
$ curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash --
$ sudo apt-get install -y nodejs
```

## nodejs version 12
```shell
$ curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash --
$ sudo apt-get install -y nodejs
```

## Vesrsion 확인

```shell
$ node -v & npm -v
```