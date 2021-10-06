# JavaScript in HTML
## 자바 스크립트를 HTML 안에서 사용하기
### 1. \<head\>안에서 실행하기
코드
``` html
<!doctype html>
<html>
    <head>
        <title>title</title>
        <link href="stylesheet.css" rel="stylesheet" type="text/css">
        <script scr="script.js"></script>
    </head>
    <body>
    </body>
</html>
```

로드순서
> HTML 파싱 → \<head>에서 JS 발견 → HTML 파싱 멈춤 → JS 패칭 → JS 실행 → 다시 HTML 파싱

단점
> 위의 로드 순서대로 JS파일이 크거나, 인터넷이 느리면 사용자가 웹 사이트르 보기까지 오래 걸림.

<br>

### 2. \<body>의 마지막에서 실행하기
코드
``` html
<html>
    <head>
        <title>title</title>
        <link href="stylesheet.css" rel="stylesheet" type="text/css">
    </head>
    <body>
        . . .
        <script scr="script.js"></script>
    </body>
</html>
```

로드순서
> HTML 파싱 → JS 발견 → JS 패칭 → JS 실행

장점
> HTML 컨텐츠를 사용자가 빠르게 볼 수 있음.

단점
> 의미있는 컨텐츠가 JS파일에 의존적이면 사용자가 기다려야 함.

<br>

### 3. \<head>안에서 async 스크립트 사용하기
코드
``` html
<html>
    <head>
        <title>title</title>
        <link href="stylesheet.css" rel="stylesheet" type="text/css">
       <script async scr="script.js"></script>
    </head>
    <body>
    </body>
</html> 
```

로드순서
> HTML 파싱 → HTML 파싱 멈춤 → 다시 HTML 파싱 → JS 파일 패칭 → JS 파일 실행

장점
> JS 패칭과 HTML 파싱이 병렬적으로 일어나서 다운로드 시간을 줄임.

단점
> JS가 HTML이 파싱되기도 전에 실행되기에 JS파일과 관련된 HTML의 요소가 파싱되지 않아 정의 되지 않았을 경우 페이지 로드의 위험이 있음.

<br>

### 4. \<head>안에서 defer 스크립트 사용하기
코드
``` html
<html>
    <head>
        <title>title</title>
        <link href="stylesheet.css" rel="stylesheet" type="text/css">
       <script defer async scr="script.js"></script>
    </head>
    <body>
    </body>
</html> 
```

로드 순서
> HTML 모두 파싱, JS 패칭 → 패칭된 JS 파일 실행

장점
> HTML 파싱과 JS패칭을 병렬로 수행한 후 마지막에 JS파일 실행