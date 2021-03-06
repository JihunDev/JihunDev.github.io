---
title: DAQ(Data Acquisition)
author: Jihun Kim
date: 2021-07-10 00:00:00 +0000
categories: [HW]
tags: [DAQ]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

# DAQ
데이터 수집(DAQ)은 전압, 전류, 온도, 압력, 소음등 전기 또는 물리적인 현상을 측정하는 과정

## DAQ 시스템 구성
Sensor - DAQ Device - Computer

- DAQ : Signal Conditioning, Analog To Digital Converter
- Computer : Driver Software, Application Software

## Sensor
- 센서는 트랜스듀서라고도 하며 물리적인 현상을 측정할 수 있는 전기 신호로 반환
- 센서 유형에 따라 전기 출력의 형태는 전압, 전류, 저항 또는 시간에 따라 변하는 다른 형태의 전기 속성 등이 될수있다

| 센서                        | 현상       |
| --------------------------- | ---------- |
| 열전쌍, RTD, 써미스터       | 온도       |
| 광센서                      | 빛         |
| 마이크                      | 소음       |
| 스트레인 게이지, 압전 센서  | 힘, 압력   |
| 전위차계, LVDT, 광학 엔코더 | 위치, 변위 |
| 가속도계                    | 가속도     |
| pH 전극                     | pH         |

## DAQ
- DAQ 디바이스는 컴퓨터와 외부 신호사이의 인터페이스 역활을 한다
- DAQ는 신호 컨디셔닝 회로, ADC, 컴퓨터 버스로 구성
- DAQ는 측정 시스템과 프로세스를 자동화 하기위한 함수도 포함
  - Ex) 디지털-아날로그 변환기(DAC)는 아날로그 신호와 디지털  I/O라인 입출력 디지털 신호를 출력하고, 카운터/타이머는 디지털 펄스로 카운팅하고 생성

### DAQ 디바이스의 주요 측정 요소
#### 신호 컨디셔닝
- 신호 또는 외부에서 수집한 신호는 노이즈가 많거나 직접 측정하기에 위험할수있다
- 신호 컨디셔닝 회로는 ADC에 입력하기 적절한 형태로 신호를 조작해준다

#### ADC
- 아날로그 신호를 디지털 형태로 변환해주는 칩
- 아날로그 신호는 시간에 따라 계속 변하며, ADC는 미리 정의된 속도로 신호의 주기적인 샘플을 수집

#### 컴퓨터 버스
- USB, PCI, PCI Express, 이더넷 등 보편적 컴퓨터 버스 형태를 제공

## Computer
- DAQ 작동을 컨트롤하고 측정 데이터를 처리, 시각화 처리 및 저장 기능