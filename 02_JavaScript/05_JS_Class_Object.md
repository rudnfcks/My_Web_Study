# JavaScript Class & Object
## 클래스와 오브젝트의 차이점
### Class ( ES6 ~ )
- 한번만 선언
- 데이터가 없음
- 정의 개념

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
↳ 클래스의 이름 출력