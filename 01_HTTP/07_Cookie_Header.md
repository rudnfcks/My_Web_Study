# Cookie Headers
## 쿠키 헤더
- Set-Cookie <br>
    서버에서 클라이언트에게 해당 쿠키를 저장하라고 명령하는 응답헤더.
    > Set-Cookie: 키=값; 옵션
    
    옵션 종류
    > - Expires: 쿠키 만료 날짜를 알림
    > - Max-Age: 쿠키 수명을 알림 (Expires는 무시됨)
    > - Secure: HTTPS에서만 쿠키가 전송
    > - HttpOnly: JS에서 쿠키에 접근할 수 없음
    > - Domain: 도메인을 적어주면 도메인이 일치하는 요청에서만 쿠키 전송
    > - Path: 패스를 적어주면 패스와 일치하는 요청에서만 쿠키 전송
<br>

- Cookie <br>
    반대로 클라이언트가 서버에게 쿠키를 보내줄때 사용하는 헤더
    > Cookie: 키=값; 키=값;