---
title: 구글 번역시 특정 부분 번역 제외 하기
author: Jihun Kim
date: 2021-11-27 00:00:00 +0000
categories: [HTML]
tags: [html]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

## **부분적으로 번역 제외하기**

해당 영역을 둘러싸고 있는 Tag에 notranslate Class를 준다.

```html
<span class="notranslate">번역하지 말아야 할 영역</span>
```

## **문서 전체를 번역 제외하기**

Html의 head 영역에 아래의 Meta 정보를 추가한다.

```html
<meta name="google" content="notranslate">
```