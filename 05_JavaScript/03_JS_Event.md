# JavaScript Use Event
## Click 이벤트 연결하기
``` javascript
const element = document.querySelector("a");

element.addEventListener("click", (e) => {
    e.preventDefault();
    console.log("is Clicked");
})
```

<br>

## Hover 이벤트 연결하기
``` javascript
const element = document.querySelector("div");

element.addEventListener("mouseenter", (e) => {
    element.style.backgroundColor = "pink";
});

element.addEventListener("mouseleave", (e) => {
    element.style.backgroundColor = "lightblue";
})
```

<br>

## 반복되는 요소에 이벤트 한거번에 연결하기
``` javascript
const list = docuemnt.qeurySelectAll("ul li");

for (let el of list) {
    el.addEventLisener("click", e => {
        console.log(e.currentTar.innerText);
    })
}
```

