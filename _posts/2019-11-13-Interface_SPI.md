---
title: SPI (Serial Peripheral Interface Bus)
author: Jihun Kim
date: 2019-11-13 20:55:00 +0800
categories: [HW, Interface]
tags: [HPI, HW]
pin: false
math: false
mermaid: false
comments: true
image:
  src: 
  alt: 
---
---

SPI Interface 설명

장치들은 Master Slave 모드로 통신하며, Master 장치는 데이터 프레임 초기화하고 여러 Slave 장치들은 개별 Slave Select라인을 통해 동작

## Interface

Signal Name  

- SCLK : 직렬 클럭(마스터로부터의 출력)
- MOSI, SIMO : 마스터 출력, 슬레이브 입력(마스터로부터의 출력)
- MISO, SOMI : 마스터 입력, 슬레이브 출력(슬레이브로부터의 출력)
- SS : 슬레이브 셀렉트(Active Low, 마스터로부터의 출력)

Alternative Names  

- SCK, CLK : 직렬 클럭(마스터부터의 입력)
- SDI, DI, DIN, SI : 직렬 데이터 입력, 데이터입력, 직렬 입력
- SDO, DO, DOUT, SO : 직렬 데이터 출력, 데이터 출력, 직렬 출력
- nCS, CS, CSB, CSB, nSS, STE : 칩 셀렉트, 슬레이브 전송 기능 이용 (Active Low, 마스터로부터의 출력)



### 간단 요약

| Signal Name | Alternative Names     | 설명                      |
| ----------- | --------------------- | ------------------------- |
| SCLK        | SCK, CLK              | Serial Clock              |
| MOSI        | SDI, DI, SI           | Master Output Slave Input |
| MISO        | SDO, DO, SO           | Slave Output Master Input |
| SS          | nCS, CS, nSS, STE, CE | Slave Select, Chip Enable |

SCLK - 단순한 동기화 신호, 통신 Clock

MOSI - Master에서 Slave로 가는 방향성이 있는 데이터 

MISO - Slave에서 Master로 가는 방향성이 있는 데이터 

SS - 하나의 Master장치가 여러개의 Slave 장치와 통신할 때 하나를 선택



## 동작구조

Circular Queue와 비슷하게 동작



## 모드 번호

| 모드 | CPOL | CPHA |
| ---- | ---- | ---- |
| 0    | 0    | 0    |
| 1    | 0    | 1    |
| 2    | 1    | 0    |
| 3    | 1    | 1    |



## SPI 장단점

### 장점

- 완전한 전이중 통신
- 전송 되는 비트에 대한 완전한 프로토콜 유연성
- 전송기가 필요하지 않음 (트랜시버 사용할 필요 없음)
- 매우 단순한 하드웨어 인터페이스 처리
- IC 패키지에 4개의 핀만 사용하며 이는 병렬 인터페이스에 비해 수가 적다



### 단점

- 하드웨어 슬레이브 인식이 없음
- 슬레이브에 의한 하드웨어 흐름 제어가 없음
- 오류 검사 프로토콜이 정의되어 있지 않음
- 일반적으로 노이즈 스파이크 영향을 받는 경향이 있음 (통신 문제를 일으킬수 있음)
- RS-232, RS-485, CAN 버스보다 비교적 더 짧은 거리에서 동작 (칩간 통신에만 이용)
- 하나의 마스터 장비만 지원