# JavaScript Element Attribute
## 속성값 알아내기
element.getAttribute(속성명);
``` javascript
console.log(element.getAttribute("herf"));
// >> https://www.naver.com
```

<br>

## 속성값 변경하기
element.setAttribute(속성명, 값);
``` javascript
element.getAttribute("herf", "https://www.google.com");
```