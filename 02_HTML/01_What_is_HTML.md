# What is HTML
## HTML 이란?
HTML ( Hypertext Markup Language ) : <br>
웹페이지가 어떻게 구조화 되어 있는지 <u>**브라우저**</u>가 알 수 있도록 하는 마크업 언어

<br>

## Tag 란?
태그( Tag )는 브라우저가 웹 문서를 잘 이해할 수 있도록 콘텐츠를 목적에 맞게 분류한 규칙이다.
``` html
<tag>내용</tag>
```
↳ 여는 태그와 닫는 태그로 이루어지며 닫는 태그는 앞쪽에 슬래시( / )를 넣어서 구분한다.

<br>

## 부모 태그와 자식 태그
태그는 들여쓰기를 이용하여 중첩관계로 제작이 가능하다.
``` html
<html>
    <head>
    </head>

    <body>
    </body>
</html>
```
↳ \<html> : 부모태그 <br>
  \<head>, \<body> : 자식태그

<br>

## HTML 기본 구조
크게 두개의 태그로 구성
> \<!DOCTYPE> : 문서 타입을 지정해주는 태그 <br>
> \<html>

<br>

\<html> 태그 안에는 \<head> 와 \<body> 태그로 나뉨.
> \<head> : 웹 브라우저에 보이지 않는 문서 설정 또는 CSS, JS 같은 외부 파일 연결 <br>
> \<body> : 다양한 HTML 태그를 이용하여 웹 브라우저에 출력할 콘텐츠 입력

<br>

index.html 파일 둘러보기

``` html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8"> // ⓐ
    <meta http-equiv="X-UA-Compatible" content="IE=edge"> // ⓑ
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> // ⓒ
    <title>Document</title> // ⓓ
</head>
<body>
    
</body>
</html>
```

### \<head> 태그 살펴보기
``` html
<meta charset="UTF-8"> // ⓐ
```
↳ 웹 문서의 인코딩 방식

<br>

``` html
<meta http-equiv="X-UA-Compatible" content="IE=edge"> // ⓑ
```
↳ 사용자가 익스플로러를 이용한다면 최신 버전인 엣지로 화면을 보여주는 기능

<br>

``` html
<meta name="viewport" content="width=device-width, initial-scale=1.0"> // ⓒ
```
↳ 디바이스 종류별로 화면에 출력할 방식 지정

<br>

``` html
<title>Document</title> // ⓓ
```
↳ 문서의 제목을 작성