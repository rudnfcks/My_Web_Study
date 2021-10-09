# JavaScript Class & Object
## 클래스와 오브젝트의 차이점
### Class ( ES6 ~ )
- 한번만 선언
- 데이터가 없음
- 정의 개념

<br>

### Object
- Class의 Instance
- 여러번 선언
- 데이터가 있음

<br>

## Class
### 클래스 선언
> 클래스는 Hoisting이 되지 않는다.
``` javascript
class name {
    constructor(var1, var2) {
        this.var1 = var1;
        this.var2 = var2;
    }
}
```

<br>

### 클래스 표현식
``` javascript
let name = class {
  constructor(var1, var2) {
    this.var1 = var1;
    this.var2 = var2;
  }
};

console.log(Rectangle.name) // >> name

let name = class name2 {
  constructor(var1, var2) {
    this.var1 = var1;
    this.var2 = var2;
  }
};

console.log(name.name); // >> name2
```
↳ 클래스로 객체( 오브젝트 ) 만들기

## 오브젝트
### 오브젝트 생성
``` javascript
var object = {};

const person = {
  name: ['Kim', 'ChanHee'],
  age: 32,
  gender: 'male',
  interests: ['music', 'skiing'],
  greeting: function() {
    alert('Hi! I\'m ' + this.name[0] + '.');
  }
};
```

<br>

### 오브젝트 사용
``` javascript
person.name
person.name[0]
person.age
person.interests[1]
person.greeting()
```

<br>

### 점 표기법
``` javascript
object.property
```

<br>

### 괄호 표기법
``` javascript
object['property']
```