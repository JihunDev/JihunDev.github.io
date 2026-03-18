---
author: Jihun Kim
categories:
- DevEnv
- Python
comments: true
date: 2021-09-25 00:00:00 +0000
math: false
mermaid: fals경
pin: false
tags:
- Python
- Mac
- brew
- TIL
title: Mac Python Version 변경
---

---

## MAC 기본 설정 되어있는 Python version 변경

    ```bash
    # 심볼릭 링크 해제
    brew unlink python
    # 심볼릭 링크 연결
    brew link --force python@{version name}
    ```