---
title: Git 다른 레파지토리 병합
author: Jihun Kim
date: 2020-07-24 00:00:00 +0000
categories: [Git]
tags: [Git]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

# 다른 레파지토리 Git병합

- 서로 다른 레파지토리 병합
- 폴더에 복사해도 넣어도 되지만 그렇게 되면 이력이 안남음

## 레파지토리 병합
```bash
$ git remote add project2 ../project2
$ git fetch project2
$ git merge --allow-unrelated-histories project2/master
$ git remote remove project2
$ git commit -m 'Merge projcet2 into project1'
$ git push
```

## .gitgnore 충돌시
```bash
$ git reset .gitgnore
```

