# Common Headers
## 공통 헤더
- Date <br>
HTTP 메시지가 만들어진 시각으로 자동으로 만들어짐.
> Date: Tue, 05 Oct 2021 04:40:06 GMT

***
<br>

- Connection <br>
사실상 아무 의미가 없는 내용으로 HTTP/2 에서부터는 아예 사라짐.
> Connection: keep-alive

***
<br>

- ***Cache-Control** <br>
추가로 다른 파일에서 정리

***
<br>

### **Content** 시리즈는 **엔티티 헤더**라 부른다.
- Content-Length <br>
요청과 음답 메시지의 본문 크기를 바이트 단위로 표시.
> Content-Length: 52

***
<br>

- Content-Type <br>
컨텐츠의 타입과 문자열 인코딩 등을 명시하는 것.
> Content-Type: text/html; charset=utf-8

***
<br>

- Content-Language <br>
사용자의 언어를 뜻하는 것으로, 요청이나 응답이 무슨 언어인지와 관계없이 표시.
> Content-Language: ko_KR

***
<br>

- Content-Encoding <br>
컨텐츠가 압축된 방식으로, br, gzip, deflate 등의 알고리즘으로 압축하여 보내면 브라우저가 알아서 해제하여 사용.
> Content-Encoding: gzip, deflate