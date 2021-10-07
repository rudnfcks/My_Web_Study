# JavaScript Variable
## 자바 스크립트의 변수선언
### 자바 스크립트 변수 선언의 종류

- var ( ~ES5 ) <br>
    변수를 선언, 추가로 동시에 값을 초기화 <br>
    > var hoisting : 선언 위치에 따라 상관없이 선언을 가장 위로 끌어올려주는 것 <br>
    > ↳ 어디에서 선언하든 var로 선언된 변수는 선언 이전에 **할당** 또는 **변조**가 가능

    - 전역 변수 선언 등 특별한 사유가 아닌 이상 거의 사용하지 않는 변수 선언

<br>

- let ( ES6 ~ ) <br>
    블록 범위 지역 변수를 선언, 추가로 동시에 값을 초기화

    - ES6 이후로 **변수**를 선언할 때 가장 많이 사용하는 변수 선언

<br>

- const <br>
    블록 범위 읽기 전용 상수를 선언

    - 변해야 하지 않고 계속 일정하거나 한번 할당 받은 값을 유지해야할 때 사용하는 변수 선언

<br>

### 변수의 사용 & 특징
1. var
    ``` javascript
    var x = 1;

    if (x === 1) {
        var x = 2;
        console.log(x); // >> expected output: 2
    }

    console.log(x); // >> expected output: 2
    ```
    > 블럭 안에서 새로 **선언 & 할당** 하였지만, 블럭 밖의 변수도 내용이 변조된 모습 <br>
    > ↳ 전역 변수의 특징을 가지고 있으며 여러번 선언이 가능함

<br>

2. let
    ``` javascript
    let x = 1;

    if (x === 1) {
        let x = 2;
        console.log(x); // >> expected output: 2
    }

    console.log(x); // >> expected output: 1
    ```
    > 블럭 안에서 새로 **선언 & 할당** 한 변수는 블럭 밖의 변수에 간섭하지 않는 모습 <br>
    > ↳ 지역번수의 특징을 가지고 있으며 같은 블럭 내에서 같은 이름의 변수를 여러번 선언이 불가능함

<br>

3. const
    ``` javascript
    const num = 5;

    try {
        num = 10;
    } catch (err) {
        console.log(err); 
        // >> expected output: expected output: TypeError: invalid assignment to const `num'
        //    Note - error messages will vary depending on browser
    }

    console.log(num); // >> expected output: 5
    ```
    > 변수를 **선언 & 할당**하고 변조하려고 하니 에러를 띄우는 모습 <br>
    > ↳ 상수의 특징을 가지고 있으며 같은 블력 내에서 같은 이름의 상수를 여러번 선언이 불가능함

<br>

## 자바스크립트의 데이터 타입
### 자바스크립트의 7가지 데이터 형
- 6가지 원시 데이터형
    - Boolean : 참, 거짓 ( 0, null, undefined, Nan, "" )
    -    null : null ( JS는 대소문자를 구별하기 때문에 null, Null, NULL 모두 다르다 )
    - undefined : 값이 저장되어 있지 않은 기본값
    - Number : 정수 또는 실수형 숫자
    - String : 문자열
    - Symbol : 인스턴스가 고유하고 불변인 데이터형
- Object