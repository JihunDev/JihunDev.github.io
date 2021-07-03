---
title: sudo -S -kS 옵션 
author: Jihun Kim
date: 2021-07-03 00:00:00 +0000
categories: [Linux, Command]
tags: [Linux, Command]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

## echo '비밀번호' | sudo -S 명령어

### Example
```shell
$ echo '1234' | sudo -S vi test.txt
```

**-S** 
- sudo가 표준입력으로부터 암호부터 읽음

## echo '비밀번호' | sudo -kS 명령어

### Example
```shell
$ echo '1234' | sudo -kS vi test.txt
```

**-kS**
- 이미 sudo가 활성화 되면 sudo에 액세스 토큰이 생성 오류발생
- 명령어를 통해 액세스 토큰 리셋

### 단점
- 관리자 권한을 얻어 실행 보안에 취약
- History에 관리자 비밀번호가 남음