# JavaScript Operators
## 자바스크립트의 연산자들

### 목차
1. [할당 연산자](#1.-할당-연산자)
2. [비교 연산자](#2.-비교-연산자)
2. [산술 연산자](#3.-산술-연산자)
2. [비트 연산자](#4.-비트-연산자)
2. [논리 연산자](#5.-논리-연산자)
2. [문자열 연산자](#6.-문자열-연산자)
2. [삼항 연산자](#7.-삼항-연산자)
2. [단항 연산자](#7.-단항-연산자)
2. [관계 연산자](#8.-관계-연산자)

<br>

### 1. 할당 연산자

이름 | 단축 연산자 | 뜻
:--- | :---: | :---:
할당 | x = y | x = y
더하기 할당 | x += y | x = x + y
빼기 할당 | x -= y | x = x - y
곱하기 할당 | x *= y | x = x * y
나누기 할당 | x /= y | x = x / y
나머지 할당 | x %= y | x = x % y
거듭제곱 할당 | x **= y | x = x ** y
왼쪽 시프트 할당 | x <<= y | x = x << y
오른쪽 시프트 할당 | x >>= y | x = x >> y
부호없는 오른쪽 시프트 할당 | x >>>= y | x = x >>> y
비트 AND 할당 | x &= y | x = x & y
비트 XOR 할당 | x ^= y | x = x ^ y
비트 OR 할당 | x \|= y | x = x \| y
논리 AND 할당 | x &&= y | x = ( x && y )
논리 OR 할당 | x \|\| = y | x = ( x \|\| y )
널 병합 할당 | x ??= y | x ?? ( x = y )

<br>

- 할당 체이닝
    ``` javascript
    let a, b, x, y;

    a = b = x = y;
    a = y; b = y; x = y;
    a = ( b = ( x = y ) );
    ```
    ↳ 3개의 코드 모두 같은 의미이다.

<br>

- 구조 분해
    ``` javascript
    var arr = ['one', 'two', 'three'];

    // 구조 분해 미사용
    var one = foo[0];
    var two = foo[1];
    var three = foo[2];

    // 구조 분해 사용
    var [one, two, three] = foo;
    ```
    ↳ 비슷한 구문을 사용해서 배열과 객체에서 데이터를 추출할 수 있는 표현식

<br>

### 2. 비교 연산자

연산자 | 부호 | 설명
:--- | :---: | :---
동등 연산자 | == | 피연산자가 서로 같으면 true 반환
부등 연산자 | != | 피연산자가 서로 다르면 true 반환
일치 연산자 | === | 피연산자의 값과 타입이 같으면 true 반환
불일치 연산자 | !== | 피연산자의 값 또는 타입이 서로 다를 경우 true 반환
보다 큼 | > | 왼쪽 피연산자가 오른쪽 피연산자보다 크면 true 반환
크거나 같음 | >= | 왼쪽 피연산자가 오른쪽 피연산자보다 크거나 같으면 true 반환
보다 작음 | < | 왼쪽 피연산자가 오른쪽 피연산자보다 작으면 true 반환
작거나 같음 | <= | 왼쪽 피연산자가 오른쪽 피연산자보다 작거나 같으면 true 반환

<br>

### 3. 산술 연산자

연산자 | 부호 | 설명
:--- | :---: | :---
더하기 | + | 이항 연산자로 두 피연산자를 더한 값을 반환
빼기 | - | 이항 연산자로 두 피연산자를 뺀 값을 반환
곱하기 | * | 이항 연산자로 두 피연산자를 곱한 값을 반환
나누기 | / | 이항 연산자로 두 피연산자를 나눈 값을 반환
나머지 | % | 이항 연산자로 두 피연산자를 나누고 나머지 값을 반환
증가 | ++ | 단항 연산자로 피연산자에 1을 더하기
감소 | -- | 단항 연산자로 피연산자에 1을 빼기
단항 부정 | - | 단항 연산자로 피연산자의 부호를 반대로 변환
단항 플러스 | + | 단항 연산자로 피연산자가 숫자타입이 아니면 숫자로 변환
거듭제곱 | ** | 이항 연산자로 첫번째 피연산자에 두번째 피연산자를 거듭제곱한 결과를 반환

<br>

### 4. 비트 연산자

연산자 | 부호 | 설명
:--- | :---: | :---
비트 AND | a & b | 두 피연산자의 각 자리 비트의 값이 모두 1인 위치에 1을 반환
비트 OR | a \| b | 두 피연산자의 각 자리 비트의 값이 모두 0인 위치에 0을 반환
비트 XOR | a ^ b | 두 피연산자의 각 자리의 비트값이 서로 다르면 0을 반환
비트 NOT | ~ a | 피연산자의 각 자리의 비트를 뒤집습니다.
왼쪽 시프트 | a << b | a의 이진 표현을 b 만큼 왼쪽으로 이동하고, 오른쪽은 0으로 채움
오른쪽 시프트 | a >> b | a의 이진 표현을 b 만큼 오른쪽으로 이동하고 1 미만으로 이동한 비트는 버림
부호없는 오른쪽 시프트 | a >>> b | a의 이진 표현을 b 만큼 오른쪽으로 이동하고 1미만으로 이동한 비트는 버리고 왼쪽은 0으로 채움

<br>

- 비트 논리 연산자 <br>
    - 기본적으로 비트 논리 연산은 최대 32비트까지만 연산이 가능하다.
    - 비트 연산은 아래와 같은 방법으로 진행된다.
        > ex ) <br>
        > 5(10) = 0101(2) <br>
        > 12(10) = 1100(2) <br>
        > 5 & 12 <br>
        > ↳ 0010 & 1100 = 0100 <br>
        > **∴ 5 & 12 = 4**

<br>

### 5. 논리 연산자

연산자 | 부호 | 설명
:--- | :---: | :---
논리 AND | && | 첫번째 피연산자와 두번째 피연산자가 모두 참 일경우 true를 반환
논리 OR | \|\| | 첫번째 피연산자 또는 두번째 피연산자가 참 일경우 true를 반환
논리 NOT | ! | 단일 피연산자가 true면 false를 false면 true를 반환

<br>

- 논리 연산자 예제
    - AND 연산자 ( && )
        ``` javascript
        console.log(true && true); // >> true
        console.log(true && false); // >> false
        console.log(false && true); // >> false
        console.log(false && (3 == 4)); // >> false
        console.log("Cat" && "Dog"); // >> Dog
        console.log(false && "Cat"); // >> false
        console.log("Cat" && false); // >> false
        ```
    
    <br>

    - OR 연산자 ( || )
        ``` javascript
        console.log(true || true); // >> true
        console.log(false || true); // >> true
        console.log(true || false); // >> true
        console.log(false || (3 == 4)); // >> false
        console.log("Cat" || "Dog"); // >> Cat
        console.log(false || "Cat"); // >> Cat
        console.log("Cat" || false); // >> Cat
        ```

    <br>

    - NOT 연산자 ( ! )
        ``` javascript
        console.log(!true); // >> false
        console.log(!false); // >> true
        console.log(!"Cat"); // >> false
        ```

<br>

### 6. 문자열 연산자
- 문자열 + 문자열
    ``` javascript
    console.log('Hello ' + 'World!'); // >> Hello World!
    ```
<br>

- 문자열 + 숫자
    ``` javascript
    console.log('Hello Num : ' + 5); // >> Hello Num : 5
    ```

<br>

- 숫자 + 문자열
    ``` javascript
    console.log(5 + ' is Number'); // >> 5 is Number
    ```

***숫자와 문자열을 더하면 숫자가 문자열로 변환되며 합쳐진다.**

- 문자열 - 숫자
    ``` javascript
    console.log('37' - 7); // >> 30
    ```
    ↳ 문자열에 더하기가 아닌 연산을 하면 숫자는 문자열로 변환되지 않는다.

### 7. 삼항 연산자
``` javascript
condition ? val1 : val2
```
↳ condition이 참이라면 val1을 반환하고 아니라면 val2를 반환

### 8. 단항 연산자
- delete <br>
    객체의 속성을 삭제하는 연산자
    ``` javascript
    delete object.property;
    delete object[propertykey];
    delete objectName[index];
    ```

- typeof <br>
    객체의 자료형을 알아내는 연산자
    ``` javascript
    typeof operand
    typeof (operand)
    ```

- void <br>
    표현식을 평가할 때 값을 반환하지 않도록 지정할 때 사용
    ``` javascript
    void expression
    void (expression)
    ```

### 9. 관계 연산자
- in <br>
    지정한 속성이 지정한 객체에 존재할경우 true를 반환
    ``` javascript
    propNameOrNumber in objectName
    ```

- instanceof <br>
    지정한 객체가 지정한 객체 타입에 속하면 true를 반환
    ``` javascript
    objectName instanceof objectType
    ```