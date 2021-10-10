# CSS Font Styling
## 폰트 굵기 바꾸기
### font-weight
속성값 | 설명
:--- | :---
nomal | 폰트를 보통 굵기로 표시
bold | 폰트를 굵게 표시

``` css
h1 {
    font-weight: normal;
}

p span {
    font-weight: bold;
}
```

<br>

## 폰트 크기 바꾸기
### font-size
속성값 | 설명
:--- | :---
px | 픽셀 단위로 폰트 크기를 설정
rem | 최상위 부모인 \<html> 태그를 기준으로 폰트 크기를 설정
em | 부모 요소를 기준으로 폰트 크기를 설정

``` css
article h1 {
    font-size: 60px;
}

article p {
    font-size: 30px;
}

article a {
    font-size: 15px;
}
```