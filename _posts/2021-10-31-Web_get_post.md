---
title: GET, POST 방식
author: Jihun Kim
date: 2021-10-31 00:00:00 +0000
categories: []
tags: []
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

# GET, POST 방식
- Select 기능을 원한다면 GET 메서드, Update 기능을 원한다면 POST 메서드
- 검색 결과 등 고정적인 주소 및 링크 주소로 사용될 수 있다면 GET 메서드를 사용
- 정보를 담을 URL길이(최대 2048자)는 한계가 있기 때문에 이를 해결하고 싶다면 POST 메소드를 사용
- POST 메서드를 쓰면 정보를 숨길 수 있다. 하지만 SSL(Secure Sockets Layer)를 사용안하면 GET과 마찬가지
- GET은 캐시가 남아있어 전송 속도가 빠르고 POST는 캐시가 남지 않아 보안적인 면에서 유리
- GET은 브라우저 히스토리에 파라미터가 남고 POST는 저장되지 않는다.
- GET은 ASCII캐릭터만 허용하나 POST는 한계가 없다. POST는 바이너리 데이터가 허용된다. 따라서 파일 입출력을 위해 POST메소드가 이용된다.