# Headers

# 공통 헤더

> 요청/응답 관계 없이 공통적으로 사용되는 헤더
> 
- Date
    
    HTTP 메시지가 만들어진 시각으로 자동으로 만들어짐.
    
    > Date: Tue, 05 Oct 2021 04:40:06 GMT
    > 
    
- Connection
    
    사실상 아무 의미가 없는 내용으로 HTTP/2 에서부터는 아예 사라짐.
    
    > Connection: keep-alive
    > 
    
- **Cache-Control**
    
    추가로 다른 파일에서 정리
    
- Content-Length
    
    요청과 음답 메시지의 본문 크기를 바이트 단위로 표시.
    
    > Content-Length: 52
    > 
    
- Content-Type
    
    컨텐츠의 타입과 문자열 인코딩 등을 명시하는 것.
    
    > Content-Type: text/html; charset=utf-8
    > 
    
- Content-Language
    
    사용자의 언어를 뜻하는 것으로, 요청이나 응답이 무슨 언어인지와 관계없이 표시.
    
    > Content-Language: ko_KR
    > 
    
- Content-Encoding
    
    컨텐츠가 압축된 방식으로, br, gzip, deflate 등의 알고리즘으로 압축하여 보내면 브라우저가 알아서 해제하여 사용.
    
    > Content-Encoding: gzip, deflate
    > 
    

# 요청 헤더

> 요청 메시지에만 포함되는 헤더
> 
- Host
    
    서버의 도메인 네임이 나타나는 부분.
    
    > Host: www.naver.com
    > 
    
- User-Agent
    
    현재 사용자가 어떤 클라이언트를 이용해 요청을 보냈는지 나타나는 부분.
    
    > User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36
    > 
    
- Accept
    
    시리즈서버에 어떠한 타입의 데이터를 보내달라고 명시하여 요청할 때 사용.
    
    > Accept: text/htmlAccept: text/html, image/pngAccept-Charset: utf-8Accept-Language: koAccept-Encoding: br, gzip
    > 
    
- Authorization
    
    인증 토큰을 서버로 보낼 때 사용.Basic 또는 Bearer와 같은 토큰의 종류를 입력 후 뒤에 토큰 문자를 작성.
    
    > Authorization: Bearer XXXXXXXXXXXXX
    > 
    
- Origin
    
    POST같은 요청을 보낼 때, 요청이 어느 주소에서 시작되었는지를 나타내는 부분.
    
- Referer현재 페이지 이전의 페이지 주소가 담겨있는 부분.
    
    > Referer: https://www.naver.com/
    > 
    

# 응답 헤더

- Access-Control-Allow-Origin요청에 서버가 허용하는 메서드와 헤더를 응답하는데 사용.Request 주소와 Response 주소가 다를경우 CORS에러 발생.
    
    > Access-Control-Allow-Origin: www.naver.com
    > 
    > 
    > access-Control-Allow-Origin: *
    > 
    
    유사한 헤더
    
    > Access-Control-Request-MethodAccess-Control-Request-HeadersAccess-Control-Allow-MethodsAccess-Control-Allow-Headers
    > 
    
- Allow
    
    Access-Control-Allow-Methods와 비슷하지만, CORS 요청 외에도 적용.GET [www.naver.com은](http://www.naver.xn--com-7e0o/) 허용하지만, POST naver.com은 허용하지 않는 경우 Allow 헤더를 설정하여 응답.
    
    > Allow: GET
    > 
    
- Content-Disposition
    
    응답 본문을 브라우저가 어떻게 표시해야 할지 설정.
    
    > Content-Disposition: inline (화면에 표시)Content-Disposition: attachment; filename='filename.txt' (다운로드)
    > 
    
- Location300
    
    또는 201 Created 응답일 경우 이동할 페이지를 설정.
    
    > HTTP/1.1 302 Found Location: /
    > 
    
- Content-Security-Policy
    
    다른 외부 파일들을 불러오는 경우, 차단할 소스와 불러올 소스를 설정.
    
    > Content-Security-Policy: default-src 'self'Content-Security-Policy: default-src https:Content-Security-Policy: default-src 'none'
    > 
    

# 캐쉬 헤더

- Cache-Control
    
    아무것도 캐싱하지 않을 경우
    
    > Cache-Control: no-store
    > 
    
    모든 캐시를 사용하기 전에 서버에게 캐시를 사용해도 되는지 여부를 확인하는 경우
    
    > Cache-Control: no-cache
    > 
    
    만료된 캐시만 서버에서 확인 받도록 하는 경우
    
    > Cache-Control: must-revalidate
    > 
    
    공유 캐시로 저장할지, 브라우저와 같은 특정 사용자 환경에만 저장할지 결정
    
    > Cache-Control: publicCache-Control: private
    > 
    
- Age
    
    캐시 응답할 때, max-age 시간 내에서 얼마나 흘렀는지 초 단위로 알림max-age=3600 일 경우 1분이 지나면 캐시 응답 해더에 생성.
    
    > Age: 60
    > 
    
- Expires
    
    Cache-Control과 별개로 응답 컨텐츠가 언제 만료되는지 표시
    
    > Expires: Tue, 05 Oct 2021 04:40:06 GMT
    > 
    
- ETag
    
    같은 주소의 자원이더라도 컨텐츠가 변경되었을 경우 ETag값이 달라짐으로써 HTTP 컨텐츠가 변경되었는지 검사가 가능
    
    > ETag: W/"3bf2-wdj3VvN8/CvXVgafkI30/TyczHk"
    > 
    
- If-None-Match
    
    서버의 ETag가 달라졌는지 검사해서 ETag가 다를 경우 컨텐츠를 새로 로드
    
    > If-None-Match: W/"3bf2-wdj3VvN8/CvXVgafkI30/TyczHk"
    > 

# 쿠키 헤더

- Set-Cookie
    
    서버에서 클라이언트에게 해당 쿠키를 저장하라고 명령하는 응답헤더.
    
    > Set-Cookie: 키=값; 옵션
    > 
    
    옵션 종류
    
    > Expires: 쿠키 만료 날짜를 알림Max-Age: 쿠키 수명을 알림 (Expires는 무시됨)Secure: HTTPS에서만 쿠키가 전송HttpOnly: JS에서 쿠키에 접근할 수 없음Domain: 도메인을 적어주면 도메인이 일치하는 요청에서만 쿠키 전송Path: 패스를 적어주면 패스와 일치하는 요청에서만 쿠키 전송
    > 

- Cookie
    
    반대로 클라이언트가 서버에게 쿠키를 보내줄때 사용하는 헤더
    
    > Cookie: 키=값; 키=값;
    > 
    

# X_로 시작하는 헤더

- X-Forwarded-For, X-Forwarded-Host, X-Forwarded-Proto요청이 어디서부터 건너왔는지 나타내는 헤더
    - For : 현재까지 거쳐온 서버의 IP 정보
    - Host : 원래 서버의 호스트명
    - Proto : 원래 서버의 프로토콜
    
    > X-Forwarded-For: 1.2.3.4, 5.6.7.8, 9.10.11.12X-Forwarded-Host: www.naver.comX-Forwarded-Proto: https
    > 
    
    표준 헤더 : Forwarded
    
    > Forwarded : for=1.2.3.4; host=www.naver.com; proto=https; by 5.6.7.8, 9.10.11.12
    > 
    
- X-Frame-Optionsframe, iframe, object 태그 안에서 페이지를 랜더링하는 것을 막을 수 있는 헤더
    
    frame, iframe, object를 안쓰는 경우
    
    > X-Frame-Option: DENY
    > 
    
    iframe 등으로 자신의 페이지를 불러오는 경우
    
    > X-Frame-Option: SAMEORIGIN
    > 
    
    특정한 사이트를 불러오는 것만 허용하는 경우
    
    > X-Frame-Option: ALLOW_FROM https://www.naver.com
    > 
    
- X-Content-Type-Option 서버에서 보내온 Content-Type 헤더가 잘못 설정되었다고 생각하는 경우 브라우저가 자체적으로 컨텐츠 타입을 추론하는 것을 허용할지 설정하는 헤더
    
    > X-Content-Type-Option: nosniff
    >