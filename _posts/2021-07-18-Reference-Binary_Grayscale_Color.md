---
title: Binary, Grayscale, Color
author: Jihun Kim
date: 2021-07-18 00:00:00 +0000
categories: [Image Processing]
tags: [Binary, Grayscale, Color]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

# Binary, Grayscale, Color
 
- Binary 
    - 1비트 0과 1, 즉 흑(0)과 백(1)으로 이루어진 영상

- Grayscale 
    - 회색조 (0....2^K-1)(8비트 영상: 0-255, 16비트 영상: 0-65535)

- Color
    - RGB, HSI (24비트 (3채널) RGB: [0...255]^2, 32비트 (4채널) CMYK: [0...255]^4)
        - RGB
            - 빨강, 초록, 파랑의 3가지 빛으로 가산혼합을 이용한 컬러모델
        - HBI
            - hue, saturation, intensity(lightness): 색상, 채도, 명도의 기본 성분으로 구성
            - 색상/색조 (Hue): 해당 색의 원색
            - 채도 (Saturation): 컬러 색의 순수도
        - CMY
            -시안(청록색)(Cyan), 마젠타(자홍색)(Magenta), 노랑(Yellow)을 기본으로 하여 감산혼합으로 컬러를 생성 (+검정(Black)(K)=CMYK)