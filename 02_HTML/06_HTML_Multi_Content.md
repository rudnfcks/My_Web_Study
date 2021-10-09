# HTML Multi Contents
웹 페이지에 비디오, 오디오 파일을 넣어 재생하기 위해 사용하는 태그

## \<audio> 태그
다양한 오디오 파일을 웹 페이지에 삽입하기 위해 사용하는 태그
``` html
<audio src="파일 위치" controls autoplay loop preload></audio>
```
종류 | 설명
:---: | :---
controls | 오디오 파일을 재생하는 컨트롤 패널을 생성
autoplay | 웹 페이지를 열면 오디오 파일을 자동으로 재생
loop | 오디오 파일을 무한 반복하여 재생
preload | 오디오 파일을 재생하기 전에 파일을 미리 불러오기

<br>

## \<video> 태그
웹 브라우저에서 동영상을 재생할 수 있게 하는 태그
``` html
<video src="파일 위치" controls autoplay loop preload></video>
```
종류 | 설명
:---: | :---
controls | 동영상 파일을 재생하는 컨트롤 패널을 생성
autoplay | 웹 페이지를 열명 동영상 파일을 자동으로 재생
loop | 동영상 파일을 무한 반복하여 재생
muted | 동영상에서 소리가 나지 않게 재생
preload | 동영상 파일을 재생하기 전에 모든 파일을 미리 불러오기
poster | 동영상 플레이어 초기 화면에 보여 줄 이미지 지정