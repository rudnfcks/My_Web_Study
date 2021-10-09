# HTML Form Tag
웹 브라우저에서 작성한 데이터를 서버로 전송하기 위해 사용하는 form 태그 사용하기
## \<input> 태그
type 속성을 다르게 지정하여 다양한 입력 형태로 만들 수 있는 태그
``` html
<label>input 요소 제목</label>
<input type="text">
```

- text 속성
    ``` html
    <label>아이디</label>
    <input type="text">
    ```

- password 속성
    ``` html
    <label>비밀번호</label>
    <input type="password">
    ```

- checkbox 속성
    ``` html
    <label>선택지</label>
    <input type="checkbox">
    ```

- radio 속성
    ``` html
    <label>선택지</label>
    <input type="radio">
    ```

- file 속성
    ``` html
    <label>파일 선택</label>
    <input type="file">
    ```

- color 속성
    ``` html
    <label>색상 선택</label>
    <input type="color">
    ```

- date 속성
    ``` html
    <label>날짜 선택</label>
    <input type="date">
    ```

- submit, reset 속성
    ``` html
    <label>전송</label>
    <input type="submit">

    <label>취소</label>
    <input type="reset">
    ```

<br>

## \<select> 태그
드롭다운 메뉴로 항목을 만들기 위해 사용하는 태그
> 자식 태그로 \<option> 사용
``` html
<select>
    <option>선택할 요소</option>
    <option>선택할 요소</option>
    <option>선택할 요소</option>
</select>
```

<br>

## \<textarea> 태그
사용자에게 텍스트를 여러 줄 입력 받을 수 있는 태그
``` html
<textarea></textarea>
```

<br>

## \<form> 태그
폼 요소를 그룹으로 만들어 한번에 벡엔드 영역으로 데이터를 전송하기 위해 사용하는 태그
``` html
<form action="전송 위치" method="전송 방법">
    <input>
    <input>
</form>
```