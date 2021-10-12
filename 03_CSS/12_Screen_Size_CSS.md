# Screen Size CSS
## 화면 너비에 따른 웹 페이지 디자인
``` css
@media screen and (max-width: 1000px) {
    실행할 CSS
}
```
↳ 웹 브라우저의 폭이 0~1000px 일때 실행할 CSS

### 사용하기
``` css
@media screen and (max-width: 1200px) {
    /* 화면 너비가 1200px 이하일 경우 보이는 CSS */
}
@media screen and (max-width: 900px) {
    /* 화면 너비가 900px 이하일 경우 보이는 CSS */
}
@media screen and (max-width: 500px) {
    /* 화면 너비가 500px 이하일 경우 보이는 CSS */
}
```

<br>

## 파비곤 아이콘 등록하고 사용하기
[파비곤 제작 웹사이트](https://favicon-generator.org)
에 접속 <br>

이미지 파일(16px × 16px) 올리고 **Create Favicon** 클릭
해당 페이지에 나오는 코드를 복사하여 사용

``` html
<link rel="shortcut icon" href="경로" type="image/x-icon">
<link rel="icon" href="경로" type="image/x-icon">
```