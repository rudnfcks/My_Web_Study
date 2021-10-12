# Interactive Content Transform
## transform 속성 이용하기
### transform ( 2D )
속성값 | 설명
:--- | :---
scale | 선택한 요소의 크기를 확대, 축소 <br> 현재 크기의 비율을 기준으로 1보다 크면 확대 작으면 축소
skewX, skewY | 선택한 요소를 x축 또는 y축으로 비틀어서 변형 <br> 원하는 각도를 정하여 기울기 조절
translate | 선택한 요소를 현재 위치 기준에서 x축 또는 y축 기준으로 이동
rotate | 선택한 요소를 회전 <br> 원하는 각도를 정하여 회전

<br>

### transform ( 3D )
속성값 | 설명
:--- | :---
rotateX, rotateY | 선택한 요소를 입체감 있게 회전
translateZ | 선택한 요소를 z 축으로 입체감 있게 보이면서 이동

<br>

### perspective
속성값 | 설명
:--- | :---
px | 3D 효과가 적용된 요소가 입체감 있게 보이도록 부모 요소에 perspective 속성을 적용하여 원근감을 부여

<br>

### transform-style
속성값 | 설명
:--- | :---
preserve-3D | 3D 효과가 적용된 요소에 모션 처리를 해도 3D 효과를 유지

<br>

### transform-origin
속성값 | 설명
:--- | :---
가로축 세로축 | 요소의 변형이 일어나는 중심축을 가로축, 세로축 기준으로 변경