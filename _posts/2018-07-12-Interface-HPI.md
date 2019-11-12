---
title: HPI (Host Port Interface)
categories:
  - Interface
  
tags: Interface

toc: true
toc_label: "On This Page"
toc_icon: "cog"
---

## HPI (Host Port Interface)
- Host Processor 와 병렬로 데이터를 주고 받을 수있는 병렬포트
- DSP는 Slave로 동작하기 때문에 Data 전송을 주도 할 수 없음
- Host Processor는 DSP Processor의 동작에 최소한 영향을 주며 DSP Processor의 내부 및 외부 메모리 액세스 가능


## HPI register 종류

### HPI Address register (HPIA)
- Host만 액세스
- Host가 액세스 하는 HPI RAM의 Address를 세트

### HPI Control register (HPIC)
- Host, C54x 쌍방 액세스
- HPI를 위한 제어 및 Status bit 포함

### HPI Data register (HPID)
- Host만 액세스
- Host는 이 register를 통해 HPI RAM에 액세스


## Host 에서 HPI 액세스 순서
1. HPIC (Control register)의 설정
2. HPIA (Address register)의 설정
3. HPID (Data register)경유에서 데이터의 read/write



## HPID 액세스 주의 사항
C54x의 on-chip RAM(HPI  RAM)의 단어 길이는 16비트이며, 상기의 레지스터도 마찬가지로 16비트이다. 

그에 대해, HPI의 버스는 8비트이므로,  호스트로부터 HPI에의 모든 액세스는 16비트를 상위/하위의 2바이트로 나누어 실시하지 않으면  안 된다. 

또한, 1회의 액세스는 반드시 2바이트 연속하여 실시할 필요가 있으며, 상위측만, 또는 하위측만의 액세스는 할 수 없다는 점에 주의해야한다.
