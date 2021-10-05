# X-Headers
## X-로 시작하는 헤더
- X-Forwarded-For, X-Forwarded-Host, X-Forwarded-Proto <br>
    요청이 어디서부터 건너왔는지 나타내는 헤더 <br>
    - For : 현재까지 거쳐온 서버의 IP 정보
    - Host : 원래 서버의 호스트명
    - Proto : 원래 서버의 프로토콜

    <br>

    > X-Forwarded-For: 1.2.3.4, 5.6.7.8, 9.10.11.12 <br>
    > X-Forwarded-Host: www.naver.com <br>
    > X-Forwarded-Proto: https

    <br>

    표준 헤더 : Forwarded 
    > Forwarded : for=1.2.3.4; host=www.naver.com; proto=https; by 5.6.7.8, 9.10.11.12

<br>

- X-Frame-Options <br>
    frame, iframe, object 태그 안에서 페이지를 랜더링하는 것을 막을 수 있는 헤더 <br>
    
    frame, iframe, object를 안쓰는 경우
    > X-Frame-Option: DENY

    iframe 등으로 자신의 페이지를 불러오는 경우
    > X-Frame-Option: SAMEORIGIN

    특정한 사이트를 불러오는 것만 허용하는 경우
    > X-Frame-Option: ALLOW_FROM
    https://www.naver.com

<br>

- X-Content-Type-Option
    서버에서 보내온 Content-Type 헤더가 잘못 설정되었다고 생각하는 경우 브라우저가 자체적으로 컨텐츠 타입을 추론하는 것을 허용할지 설정하는 헤더

    > X-Content-Type-Option: nosniff