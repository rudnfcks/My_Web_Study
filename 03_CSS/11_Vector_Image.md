# Use Vector Image
## 비트맵 이미지와 벡터 이미지의 차이
비트맵 이미지 | 벡터 이미지
:--- | :---
수많은 픽셀을 조합해 이미지를 출력 | 좟푯값을 연결하여 이미지를 출력
확대 시 이미지 품질의 저하 | 확대 하더라도 이미지 품질 유지
큰 파일 용량 | 비트맵 보다 작은 파일 용량

<br>

## SVG 파일을 웹 브라우저에 출력하기
SVG 파일 형식 <br>
파일명.SVG

```
<svg>
    <path>
    </path>
</svg>
```
### 이미지 사용과 똑같이 사용하기

``` html
<img src="파일명.SVG" alt="설명">
```

<br>

### 태그 가져와서 사용하기
위 태그를 복사해서 svg 태그로 사용하기
``` html
<svg>
    <path>
    </path>
</svg>
```

<br>

## SVG의 path 스타일 변경하기
### fill
속성값 | 설명
:--- | :---
색상, transparent | svg의 색상을 변경

<br>

### stroke
속성값 | 설명
:--- | :---
색상 | svg의 테두리 색상을 변경

<br>

### stroke-width
속성값 | 설명
:--- | :---
비율 | 테두리 굵기를 설정
|| 1보다 크면 굵게 작으면 얇게 설정

<br>

## SVG의 viewBox 속성 사용하기
### viewBox
속성값 | 설명
:--- | :---
x y width height | svg 내에서 그려질 위치와 크기를 설정

<br>

## path의 stroke 속성 사용하기
### stroke-dasharray
선의 간격을 띄는 속성 <br>
( 이미 그려진 선을 입력 값 만큼 임의로 자르기 )

<br>

### stroke-dashoffset
가시 영역에 보이는 선의 시작 위치를 지정하는 속성 <br>
( stroke-dashoffset으로 자른 간격에서부터 선이 시작되는 위치를 설정)