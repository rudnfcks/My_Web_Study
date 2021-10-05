# HTTP Method
## HTTP 메서드란?
**요청**할 때, 해당 주소에 대한 어떤 동작을 하려고 할때 해당하는 동작이 무엇인지 알려주는 요소
> ex ) GET　www．naver．com HTTP/1.1

## HTTP 메서드
- GET - 가져오기
- POST - 게시하기
- PUT - 집어넣기
- PATCH - 고치기
- DELETE - 지우기
- OPTIONS - 옵션
- HEAD - 헤더
- CONNECT - 연결하기
- TRACE - 교환하기

REST : 주소를 **자원**으로, 메서드를 **동사**로 보는 개발 방식

> 메서드 사용하기 ex ) <br>
GET /users HTTP/1.1 : 사용자들의 정보 가져오기 <br>
DELETE /users/5 HTTP/1.1 : 아이디가 5인 사용자를 삭제하기

> Parameters 전달하기 ex ) <br>
GET /users?sort=name HTTP/1.1 <br>
GET /users?sort=name&filter=developer HTTP/1.1

<br>

## 주로 사용되는 메서드
- GET <br>
서버에게 응답 요청하기
> ex ) *GET 주소 HTTP/1.1* : <br>
요청에 표시되어야 할 정보 전달

- POST <br>
서버에게 응답과 생성을 요청하기
> ex ) *POST 주소 HTTP/1.1* : <br>
새로운 정보 생성(등록) 또는 업로드

- PUT <br>
서버에게 응답을 업데이트 하거나 응답이 없다면 생성을 요청하기
> ex ) *PUT 주소 HTTP/1.1* : <br>
해당 데이터가 없으면 생성, 있다면 전체를 변경하기

- PATCH <br>
서버에게 응답의 업데이트를 요청하기
> ex ) *PATCH 주소 HTTP/1.1* : <br>
변화가 있는 데이터를 변경하기

- DELETE <br>
서버에게 응답의 삭제를 요청하기
> ex ) *DELETE 주소 HTTP/1.1* : <br>
응답을 삭제하기

<br>

## 주로 사용되지 않는 메서드
- HEAD <br>
요청에서 **헤더**만 가져오기
> ex ) *HEAD 주소 HTTP/1.1* : <br>
*GET 주소 HTTP/1.1* 요청 후 헤더만 받아오기

- OPTION <br>
서버가 어떤 메서드를 지원하는지 확인하기
> ex ) *OPTION 주소 HTTP/1.1* : <br>
사용가능한 메서드 응답 (GET, HEAD)

<br>

## 거의 사용되지 않는 메서드
- TRACE <br>
핑퐁 테스트

- CONNECT <br>
양방향 통신