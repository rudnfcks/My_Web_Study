# Cache Headers
## 캐시 헤더
- Cache-Control <br>
    아무것도 캐싱하지 않을 경우
    > Cache-Control: no-store
    
    모든 캐시를 사용하기 전에 서버에게 캐시를 사용해도 되는지 여부를 확인하는 경우
    > Cache-Control: no-cache

    만료된 캐시만 서버에서 확인 받도록 하는 경우
    > Cache-Control: must-revalidate

    공유 캐시로 저장할지, 브라우저와 같은 특정 사용자 환경에만 저장할지 결정
    > Cache-Control: public <br>
    > Cache-Control: private

<br>

- Age <br>
    캐시 응답할 때, max-age 시간 내에서 얼마나 흘렀는지 초 단위로 알림  <br>
    max-age=3600 일 경우 1분이 지나면 캐시 응답 해더에 생성.
    > Age: 60

<br>

- Expires <br>
    Cache-Control과 별개로 응답 컨텐츠가 언제 만료되는지 표시
    > Expires: Tue, 05 Oct 2021 04:40:06 GMT

<br>

- ETag <br>
    같은 주소의 자원이더라도 컨텐츠가 변경되었을 경우 ETag값이 달라짐으로써 HTTP 컨텐츠가 변경되었는지 검사가 가능
    > ETag: W/"3bf2-wdj3VvN8/CvXVgafkI30/TyczHk"

<br>

- If-None-Match <br>
    서버의 ETag가 달라졌는지 검사해서 ETag가 다를 경우 컨텐츠를 새로 로드
    > If-None-Match: W/"3bf2-wdj3VvN8/CvXVgafkI30/TyczHk"