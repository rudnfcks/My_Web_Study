# Auto Work Animation Effect
## animation 속성을 이용하여 자동으로 움직이는 애니메이션 만들기
### @keyframes
속성값 : 애니메이션 세트 지정 <br>
설명 :
- 애니메이션의 시작과 끝을 등록하여 사용자 모션을 등록
- 0%는 시작 지점이고 100%는 끝 지점을 의미
- 중간 지점은 여러개 추가 가능
- 단계별로 동작 방식을 지정해서 특정 이름을 붙여 키프레임 등록 가능

<br>

### animation-name
속성값 | 설명
:--- | :---
이름 | 키프레임으로 등록한 모션의 이름을 호출

<br>

### animation-duration
속성값 | 설명
:--- | :---
지속시간 | 키프레임 모션 한 세트를 얼마 동안 동작하게 할지 초 단위로 등록

<br>

### animation-timing-function
속성값 | 설명
:--- | :---
가속도 | 키프레임 모션을 실행할 때 가속도 설정

<br>

### animation-delay
속성값 | 설명
:--- | :---
지연 시간(초 단위) | 키프레임 모션을 실행할 때 지연시간 설정

<br>

### animation-play-state
속성값 | 설명
:--- | :---
running, paused | 키프레임 모션을 실행할 때 동작 상태 지정

<br>

### animation
속성값 | 설명
:--- | :---
이름 / 진행시간 / 가속도 / 지연시간 / 반복횟수 | 애니메이션 축약