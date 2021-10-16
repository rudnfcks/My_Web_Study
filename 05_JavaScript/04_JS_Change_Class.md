# JavaScript Changed Class
## 자바 스크립트로 클래스 제어하기
### 클래스를 제어하는 이유
- 스타일을 자바스크립트로 변경할 경우 CSS가 변하는 것이 아닌 요소에 Style 속성이 생김
- Style을 직접적으로 변경할 경우 무엇이 어떻게 변하는지 확인하기 어려워짐
- 공통적인 Style을 여러 요소에 부여할 때 가독성이 떨어짐

↳ 클래스에 Style을 넣고 해당 클래스를 요소에 넣어서 Style을 제어

<br>

### classList
``` javascript
element.addEventListener("click", () => {
    element.classList.add("on");
})
```
↳ .on 클래스를 [ Background-color: red ]로 설정했을 경우 요소를 클릭하면 요소가 빨간색으로 변경됨

<br>

``` javascript
element.addEventListener("click", () => {
    element.classList.remove("on");
})
```
↳ 기본 요소가 [ background-color: blue ]로 설정되어 있고 on클래스가 [ backgorund-color: red ]라서 빨간색으로 보일경우 요소를 클릭하면 파란색으로 변경됨

