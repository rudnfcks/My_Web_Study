# HTTP란?

### HTTP 이전에..

> 프로토콜 : 규칙, 방식, 규격

**인터넷 프로토콜 스위트** (Internet Protocol Suite) :

인터넷에서 컴퓨터들이 서로 정보를 주고받는데 쓰이는 프로토콜의 모음 (TCP, IP, TCP/IP ...)

**패킷 통신 방식의 인터넷 프로토콜, IP :**

패킷 전달 여부를 보증하지 않고, 패킷을 보낸 순서와 받는 순서가 다를 수 있는 프로토콜

**전송 조절 프로토콜, TCP :**

데이터의 전달을 보증하고, 보낸 순서대로 받게 해주는 IP 위에서 작동하는 프로토콜

**TCP/IP :**

IP와 TCP로 이루어진 프로토콜로, 많은 인터넷 프로토콜의 기반이 되는 프로토콜

# ❓ HTTP란

**HTTP (Hyper Text Transfer Protocol) :**

인터넷에서 데이터를 주고받을 수 있는 프로토콜로, TCP/IP기반 프로토콜이다.

# ✉ 메시지 포맷

메시지 포맷의 2가지

## 요청 (Request)

> 클라이언트가 서버에게 해당 주소의 정보를 요청

요청 정보의 구조

- 시작줄 - 메서드 주소 버전
  (ex. GET /image/logo.gif HTTP/1.1
- 헤더 - 요청에 대한 정보
  (ex. Accept-Language: en)
- 빈 줄 (empty line)
- 본문 - 데이터 - 기타 메시지

## 응답 (Response)

> 서버가 클라이언트에게 요청에 맞는 정보를 전달

응답 정보의 구조

- 시작줄 - 버전, 상태코드, 상태 메시지
- 헤더 - 응답에 대한 정보
- 빈 줄 (empty line)
- 본문 - 데이터 - 기타메시지

# 헤더 종류 알아보기

[Headers](https://github.com/rudnfcks/My_Web_Study/blob/main/01_Internet/Headers.md)
