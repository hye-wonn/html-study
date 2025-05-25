# 1. 폼 태그 (`<form>`)

## 1-1. 폼 태그란?

-   사용자 입력을 수집하여 서버로 전송하는 HTML 태그
-   다양한 입력 필드(`<input>`, `<textarea>`, `<select>` 등)와 함께 사용

## 1-2. 주요 속성

-   `action`: 데이터를 전송할 서버 URL 지정
-   `method`: 전송 방식 (GET 또는 POST)
-   `enctype`: 전송 시 데이터 인코딩(암호화) 방식 지정 (`method = "post"`인 경우에만 사용 가능)
    -   application/x-www-form-urlencoded (기본값, 모두 인코딩)
    -   multipart/form-data (파일이나 이미지 전송, 모두 인코딩 X)
-   `target`: 폼 제출 결과 표시 위치 지정 (`_self`, `_blank`, `_parent`, `_top`, etc.)

> 💡 추가 설명
>
> -   `GET`: URL에 데이터 포함 → 검색, 필터 등 비민감한 데이터 전송에 적합
> -   `POST`: 본문(body)에 데이터 포함 → 로그인, 회원가입 등 보안 필요한 전송에 적합

## 1-3. 폼 태그 사용 예시

```html
<form action="/submit" method="POST" enctype="multipart/form-data" target="_self">
    <label for="username">사용자 이름:</label>
    <input type="text" id="username" name="username" required />
    <button type="submit">제출</button>
</form>
```
