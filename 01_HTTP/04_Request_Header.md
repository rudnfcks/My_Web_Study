# Request Headers
## 요청 헤더
- Host <br>
서버의 도메인 네임이 나타나는 부분.
    > Host: www.naver.com

<br>

- User-Agent <br>
현재 사용자가 어떤 클라이언트를 이용해 요청을 보냈는지 나타나는 부분.
    > User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36

<br>

- Accept 시리즈<br>
서버에 어떠한 타입의 데이터를 보내달라고 명시하여 요청할 때 사용.
    > Accept: text/html <br>
    > Accept: text/html, image/png <br> <br>
    > Accept-Charset: utf-8 <br>
    > Accept-Language: ko <br>
    > Accept-Encoding: br, gzip
 
<br>

- Authorization <br>
인증 토큰을 서버로 보낼 때 사용. <br>
Basic 또는 Bearer와 같은 토큰의 종류를 입력 후 뒤에 토큰 문자를 작성.
    > Authorization: Bearer XXXXXXXXXXXXX

<br>

- Origin <br>
POST같은 요청을 보낼 때, 요청이 어느 주소에서 시작되었는지를 나타내는 부분.

<br>

- Referer <br>
현재 페이지 이전의 페이지 주소가 담겨있는 부분.
    > Referer: https://www.naver.com/