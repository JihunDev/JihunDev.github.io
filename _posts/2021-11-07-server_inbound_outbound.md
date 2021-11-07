---
title: Inbound, Outbound란
author: Jihun Kim
date: 2021-11-07 00:00:00 +0000
categories: [Server]
tags: [Server]
comments: true
pin: false
math: false
mermaid: false
image:
  src:
  alt:
---
---

- Inbound
    - 외부에서 가상서버 내부로 데이터가 유입될때 발생하는 트래픽
    - e.g.
        - 클라이언트가 웹사이트에 접속했을 경우 클라이언트의 접속정보가 가상서버 내의 DB에 저장된다거나 클라이언트가 웹사이트에서 어떠한 정보가 필요하여 가상서버에 요청 데이터를 보냈을 경우
        - FTP나 웹사이트 첨부파일 등으로 가성서보내로 파일을 전송하는 경우
- Outbound
    - 가성서버 내에서 외부로 데이터가 전송되었을때 발생하는 트래픽
    - e.g.
        - 클라이언트가 웹사이트에서 어떤 정보를 요청하였을 때 해당 정보에 대한 데이터를 다시 클라이언트로 전송시 발생된 트래픽
        - FTP나 웹사이트에서 클라이언트 PC로 파일 다운로드 하는 경우
- Inbound, Outbound의 트래픽이 발생되는 요소는 다양