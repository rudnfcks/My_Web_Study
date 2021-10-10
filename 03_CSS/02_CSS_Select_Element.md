# CSS Select Elements
## CSS의 기본적인 형태
``` css
h1 {
    color: red;
}
```
- h1 : 선택자
- color : 속성명
- red : 속성값

<br>

## CSS 선택자
### 1. 전체 선택자
모든 HTML 요소를 한꺼번에 선택하기
``` css
* {
    border: 1px solid red;
}
```

<br>

### 2. 태그 선택자
태그명을 이용하여 선택하기
``` css
h1 {
    border: 1px solid red;
}

h2 {
    border: 1px solid green;
}

h3 {
    border: 1px solid blue;
}
```

<br>

### 3. 자손 선택자
자식과 하위 요소를 모두 선택하기
``` css
p strong {
    border: 1px solid blue;
}
```

<br>

### 4. 자식 선택자
직계 자식 요소만 선택하기
``` css
ul > li {
    border: 1px solid blue;
}
```

<br>

### 5. 그룹 선택자
여러 개의 요소를 그룹으로 선택하기
``` css 
h1, h2, h3 {
    border: 1px solid blue;
}
```

<br>

### 6. 순서 선택자
형제 요소의 순서를 이용하여 선택하기
``` css
ul li:nth-of-type(1) {
    border: 1px solid red;
}

ul li:nth-of-type(2) {
    border: 1px solid green;
}

ul li:nth-of-type(3) {
    border: 1px solid blue;
}

ul li:nth-of-type(4) {
    border: 1px solid violet;
}
```

<br>

### 7. 수열 선택자
수식을 이용하여 선택하기
``` css
ul li:nth-of-type(2n) {
    border: 1px solid blue;
}
```

<br>

### 8. 마지막 요소 선택자
형제 요소 중 마지막 요소를 선택하기
``` css
ul li:last-chile {
    border: 1px solid blue;
}
```

<br>

### 9. 홀수, 짝수 선택자
홀수 또는 짝수 요소를 선택하기
``` css
ul li:nth-of-type(odd) {
    border: 1px solid blue;
}
ul li:nth-of-type(even) {
    border: 1px solid red;
}
```

<br>

### 10. 속성 선택자
속성 값을 이용해서 선택하기
``` css
input[type="text"] {
    border: 1px solid blue;
}
input[type="password"] {
    border: 1px solid red;
}
```

<br>

### 11. 가상 선택자
가상의 요소를 선택하기
``` css
h1 {
    border: 1px solid blue;
}

h1:hover {
    border: 1px solid red;
}

h2:before {
    content: "before content";
    color: blue;
}

h2:after {
    content: "after content";
    color: red;
}
```

<br>

### 12. 클래스, 아이디 선택자
HTML에서 클래스, 아이디 선택자 만들기
``` html
<p class="클래스명"> </p>
<p id="아이디명"> </p>
```

<br>

클래스 명, 아이디 명으로 요소 선택하기
``` css
p.text1 {
    border: 1px solid blue;
}

.text2 {
    border: 1px solid red;
}

#header {
    border: 1px solid red;
}

#section {
    border: 1px solid green;
}

#footer {
    border: 1px solid violet;
}
```