---
author: Jihun Kim
categories:
- DevEnv
- Docker
comments: true
date: 2019-11-08 20:55:00 +0800
image:
  alt: DockerJekyll
  path: https://i.imgur.com/fpPqT7O.png
math: false
mermaid: false
pin: false
tags:
- Docker
- Jekyll
- Blog
- Setup
title: Docker로 Jekyll 사용
---

---

Docker로 Jekyll 사용하여 홈페이지 관리

## Docker에 Jekyll 설치
```shell
$ docker pull jekyll/jekyll
```

## Docker Jekyll 실행
```shell
$ docker run --volume="$PWD:/src/jekyll" -p 4000:4000 -it jekyll/jekyll jekyll serve
```

## 접속 방법
접속 URL : http://0.0.0.0:4000/

## reference
[DockerHub-jekyll](https://hub.docker.com/r/jekyll/jekyll/)

[Running Jekyll in Docker](https://ddewaele.github.io/running-jekyll-in-docker/)