---
title: AWS Nginx 413 Request Entity Too Large Err
author: Jihun Kim
date: 2021-09-20 00:00:00 +0000
categories: [AWS, Nginx]
tags: [AWS, Nginx]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

# Info

- Nginx의 기본 File Upload 크기는 1mb이며 이를 초과하면 Err가 발생
    - 개발서버에서는 오류가 안나고 실서버 운영에서만 발생

# Solution

- platform/nginx/conf.d에 custom 옵션을 넣어줌

```python
~/workspace/my-app/
|-- .platform
|   `-- nginx
|       `-- conf.d
|           `-- myconf.conf
`-- other source files
```

```python
# myconf.conf
client_max_body_size 50M;
```