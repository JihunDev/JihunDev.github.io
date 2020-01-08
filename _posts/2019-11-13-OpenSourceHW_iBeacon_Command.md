---
layout: post
title: iBeacon 만들기
tags: Beacon
comments: true
---

iBeacon 만드는 비콘 명령어

## H/W
* HM-10 Bleutooth
* FTDI

## S/W
* [Hercules](https://www.hw-group.com/products/hercules/index_en.html)

## Pin Map

| FTDI | HM-10 |
|--|--|
| VCC | VCC |
| GND | GND |
| RX | TX |
| TX | RX |

## AT Command Setting
### 01 AT

```
AT
Ok
```

### 02 AT+RENEW

HM-10 공장초기화  

```
AT+RENEW
OK+RENEW
```

### 03 AT+RESET

HM-10 재부팅    

```
AT+RESET
OK+RESET
```

### 04 AT

AT 모드 응답확인

```
AT
OK
```

### 05 AT+MARJ0x1234 

Major Number 설정 (16진수)
사용자 정의 대로 변경가능

```
AT+MARJ0x1234
OK+Set:0x1234
```

### 06 AT+MINO0xFA01 

Minor Number 설정 (16진수)
사용자 정의 대로 변경가능

```
AT+MINO0xFA01
OK+Set:0xFA01
```

### 07 AT+ADVI5

신호 5초 간격으로 송출 

```
AT+ADVI5
OK+Set:5
```

### 08 AT+NAMEIBEACON

HC-10의 이름을 IBEACON으로 설정
IBEACON의 이름은 사용자 정의 대로 변경가능

```
AT+NAMEIBEACON
OK+Set:IBEACON
```

### 09 AT+ADTY3

Non-Connectable 상태 (절전 효과)    

```
AT+ADTY3
OK+Set:3
```

### 10 AT+IBEA1

HM-10을 iBeacon모드 변경

```
AT+IBEA1
OK+Set:1
```

### 11 AT+DELO2

HM-10을 Broadcast 전용 모드 설정 (절전 효과)

```
AT+DELO2
OK+DELO2  
```

### 12 AT+PWRM0

HM-10을 Auto-Sleep모드 설정 (절전 효과)
```
AT+PWRM0
OK+Set:0
```

### 13 AT+RESET
HM-10 재부팅   

```
AT+RESET
OK+RESET
```

## Troubleshooting

### Auto-Sleep 모드 해제
아무 문자나 80자 이상 입력 

```
OK-WAKE
```
