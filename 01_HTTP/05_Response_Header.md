# Request Headers
## 응답 헤더
- Access-Control-Allow-Origin <br>
요청에 서버가 허용하는 메서드와 헤더를 응답하는데 사용. <br>
Request 주소와 Response 주소가 다를경우 CORS에러 발생.
    > Access-Control-Allow-Origin: www.naver.com <br>
    > access-Control-Allow-Origin: *

    유사한 헤더
    > Access-Control-Request-Method <br>
    > Access-Control-Request-Headers <br>
    > Access-Control-Allow-Methods <br>
    > Access-Control-Allow-Headers <br>

<br>

- Allow <br>
Access-Control-Allow-Methods와 비슷하지만, CORS 요청 외에도 적용. <br>
GET www.naver.com은 허용하지만, POST naver.com은 허용하지 않는 경우 Allow 헤더를 설정하여 응답.
    > Allow: GET <br>

<br>

- Content-Disposition <br>
응답 본문을 브라우저가 어떻게 표시해야 할지 설정.
    > Content-Disposition: inline (화면에 표시) <br>
    > Content-Disposition: attachment; filename='filename.txt' (다운로드)

<br>

- Location <br>
300 또는 201 Created 응답일 경우 이동할 페이지를 설정.
    > HTTP/1.1 302 Found
    > Location: /

<br>

- Content-Security-Policy <br>
다른 외부 파일들을 불러오는 경우, 차단할 소스와 불러올 소스를 설정.
    > Content-Security-Policy: default-src 'self' <br>
    > Content-Security-Policy: default-src https: <br>
    > Content-Security-Policy: default-src 'none'

