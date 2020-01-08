---
layout: post
title: Docker로 Jekyll 사용
tags: Docker Jekyll
comments: true
---

Docker로 Jekyll 사용하여 홈페이지 관리

![Docker/Jekyll](https://i.imgur.com/fpPqT7O.png)

## 처음 Jekyll 사용자
(추후 업데이트)

## 기존 Jekyll 사용자

### Docker에 Jekyll 설치
```shell
$ docker pull jekyll/jekyll
```

### Docker Jekyll 실행
```shell
$ docker run --volume="$PWD:/src/jekyll" -p 4000:4000 -it jekyll/jekyll jekyll serve
```

### 접속 방법
접속 URL : http://0.0.0.0:4000/

## reference
[DockerHub-jekyll](https://hub.docker.com/r/jekyll/jekyll/)
[Running Jekyll in Docker](https://ddewaele.github.io/running-jekyll-in-docker/)