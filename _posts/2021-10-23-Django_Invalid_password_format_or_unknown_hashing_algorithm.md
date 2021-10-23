---
title: Django Invalid password format or unknown hashing algorithm
author: Jihun Kim
date: 2021-10-23 00:00:00 +0000
categories: [Django]
tags: [Django]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

- django를 통해 회워가입을 구현할 때 당면할 수 있는 문제
- 유효하지않은 패스워드 형식이거나 해싱 알고리즘이 이상할 경우 생겨나는 문제이다.

DRF를 사용하고 serializer를 통해 회원가입 프로세스를 진행할 경우:

```
user = serializer.save()
user.set_password('request['password']')
user.save()
```

User를 통해 진행할 경우:

```
user = User.objects.create_user('john', 'john@test.com')
user.set_password(request['password'])
user.save()
```

- set_password() 는 save()를 자동으로 안하기 떄문에 마지막에 save()를 통해서 바뀌어진 비밀번호를 명시