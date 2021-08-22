---
title: 자주 쓰는 Git Command
author: Jihun Kim
date: 2021-08-22 00:00:00 +0000
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
# 자주 쓰는 Git Command

## Clone

```
git clone {url} : 프로젝트 Clone
git clone -b {branch_name} --single-branch {저장소 URL} : 원격 저장소의 특정 branch만 clone
```

## Branch

```
git branch {name} : name branch를 생성
git checkout {branch_name} : 특정 로컬 branch로 전환
git checkout -r {branch_name} : 특정 원격 branch로 전환
git branch -r : 원격 저장소의 branch 목록 조회
git branch -a : 로컬 저장소의 branch 목록 조회
git branch -m {current_name} {change_name} : branch 이름 변경
git branch -d {branch_name} : 특정 branch 삭제
```

## Commit

```
git status : staging 현황
git add {file} : file을 staging
git add * : 변경된 모든 파일을 staging
git commit -m "": staging된 파일들을 commit
```

## Push

```
git push : 현재 branch를 push
git push {branch_name} : 로컬 저장소의 특정 branch에 push
git push {remote_name} {branch_name} : 원격 저장소의 특정 branch에 push
```

## Pull/fetch

```
git pull : 현재 branch의 변경사항 가져오기
git fetch {remote_name} : 원격 저장소의 변경사항 가져오기
git pull {remote_name} {branch_name}: 원격 저장소 특정 branch와 merge 방식으로 병합
git pull --rebase {remote_name} {branch_name} : 원격 저장소 특정 branch와 rebase 방식으로 병합
```

## Repository

```
git init : 새로운 저장소 생성
```

## Remote

```
git remote add origin 링크 : 원격 저장소를 설정
```