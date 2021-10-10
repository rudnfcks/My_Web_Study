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
### 전체 선택자
모든 HTML 요소를 한꺼번에 선택하기
``` css
* {
    border: 1px solid red;
}
```

<br>

### 태그 선택자
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

### 자손 선택자
자식과 하위 요소를 모두 선택하기
``` css
p strong {
    border: 1px solid blue;
}
```

<br>

### 자식 선택자
직계 자식 요소만 선택하기
``` css
ul > li {
    border: 1px solid blue;
}
```

<br>

### 그룹 선택자
여러 개의 요소를 그룹으로 선택하기
``` css 
h1, h2, h3 {
    border: 1px solid blue;
}
```

<br>

### 순서 선택자
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

### 수열 선택자
수식을 이용하여 선택하기
``` css
ul li:nth-of-type(2n) {
    border: 1px solid blue;
}
```

<br>

### 마지막 요소 선택자
형제 요소 중 마지막 요소를 선택하기
``` css
ul li:last-chile {
    border: 1px solid blue;
}
```