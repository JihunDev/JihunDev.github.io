---
layout: post
title: 서로 다른 Repositories 병합
tags: Git
comments: true
---

다른 레파지토리 Git병합 방법

- 서로 다른 레파지토리 병합
- 폴더에 복사해도 넣어도 되지만 그렇게 되면 이력이 안남음

## 레파지토리 병합

```shell
$ git remote add project2 ../project2
$ git fetch project2
$ git merge --allow-unrelated-histories project2/master
$ git remote remove project2
$ git commit -m 'Merge projcet2 into project1'
$ git push
```



## .gitgnore 충돌시

```shell
$ git reset .gitgnore
```
