# JavaScript Function
## 자바 스크립트의 함수 정의
### 함수 선언 ( function 문 )
기본적으로 알고 있는 함수 선언문
``` javascript
function name([param[, param[, ... param]]]) {
    statements
}
```
- name : 함수이름
- param : 함수에 전달되는 인수의 이름
- statements : 함수의 몸통을 구성하는 문.

<br>

### 함수 표현식 ( function 식 )
함수를 변수에 담을 수 있는 함수 정의식
``` javascript
function [name]([param[, param[, ... param]]]) {
    statements
}
```
- name : 함수이름. 함수가 익명 함수로 알려진 경우 생략 가능
- param : 함수에 전달되는 인수의 이름
- statements : 함수의 몸통을 구성하는 문

``` javascript
var myFunction = function() {
    statements
}
```
``` javascript
var myFunction = function namedFunction() {
    statements
}
```
``` javascript
(function() {
    statements
})();
```
↳ 함수 선언하고 실행하는 것이 아닌, 선언과 동시에 실행하는 문

<br>

### 생성기 함수 선언 ( function* 문 )
생성기( Generator ) 함수로 iterator 객체가 반환되는 함수
``` javascript
function* namedFunction([param[, param[, ... param]]]) {
    statements
}
```

Generator 함수 이해하기
``` javascript
function* generator(i) {
    yield i;
    yield i + 10;
}

const gen = generator(10);

console.log(gen.next().value); // >> 10
console.log(gen.next().value); // >> 20
console.log(gen.next().value); // >> undefined
```
↳ Generator 함수는 혼자서 실행되지 못한다. ( 함수로 반환되는 객체를 변수로 받아서 사용) <br>
↳ yield 로 반환하는 값이 iterator에 차례대로 저장됨 <br>
↳ 객체.next().value 를 통해 iterator에 저장된 값을 차례로 추출

<br>

### 생성기 함수 식 ( function* 식 )
위 Generator Function의 함수식 버전
``` javascript
function* [name]([param[, param[, ... param]]]) {
   statements
}
```

<br>

### 화살표 함수 표현식 ( => )
구문이 더 짧고 어휘상 this 값을 바인딩 하는 함수
``` javascript
([param[, param]]) => {
   statements
}

param => expression
```
- param : 인수의 이름. 0개의 인수는 ()로 표시
- statements or expression : 선언문. 여러개일 경우 중괄호로 묶음