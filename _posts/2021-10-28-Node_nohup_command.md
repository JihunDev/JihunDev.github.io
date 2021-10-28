---
title: Node nohup Command
author: Jihun Kim
date: 2021-10-28 00:00:00 +0000
categories: [Node.js]
tags: [Node.js]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

# 실행 방법

```bash
$ nohup node /경로/main.js &
```

1. 일반 실행 방법
 - 일반적인 실행 방법으로는 ssh가 묶여 다른 작업을 할 수 없음
 
 ```bash
 $ node server.js
 ```
    
2. Background 실행 방법
 - Background Process로 실행되어 ssh에서 다른 작업을 할 수 있음
 
 ```bash
 $ nohup node server.js &
 ```
    

# 실행 확인 방법

```bash
$ ps -aux | grep server.js
```

# 중지 방법

```bash
$ ps -ef | grep a.out
$ kill -9 pid번호
```

# PS

- nohup 사용시 사용 디렉토리에 nohup.out이라는 파일이 자동 생성됨
- nohup.out에는 nohup사용시 출력이 기록됨
- nohup.out 사용하고 싶지 않다면

```bash
$ nohup echo hello > /dev/null
```