# 2. 입력 태그

## 2-1. `<input>` 태그

### 2-1-1. `<input>` 태그란?

-   한 줄짜리 입력 필드를 생성
-   type 속성에 따라 다양한 입력 방식 지원

### 2-1-2. 주요 속성

-   `type`: 입력 유형 지정 (e.g. text, password, email, number, file, etc.)
-   `name`: 서버로 전송될 데이터의 키 이름
-   `value`: 입력 필드 초기값
-   `placeholder`: 입력 전 표시되는 안내 텍스트
-   `required`: 필수 입력 필드로 설정

### 2-1-3. `<input>` 태그 사용 예시

```html
<input type="email" name="email" placeholder="이메일 입력" required />
```

## 2-2. `<textarea>` 태그

### 2-2-1. `<textarea>` 태그란?

-   여러 줄 입력이 가능한 텍스트 필드 생성

### 2-2-2. 주요 속성

-   `name`: 서버로 전송될 데이터의 키 이름
-   `rows`: 기본 행 수
-   `cols`: 기본 열 수
-   `placeholder`: 안내 텍스트

### 2-2-3. `<textarea>` 태그 사용 예시

```html
<textarea name="comments" rows="4" cols="50" placeholder="의견을 입력하세요"></textarea>
```

## 2-3. `<button>` 태그

### 2-3-1. `<button>` 태그란?

-   폼 제출, 초기화 또는 일반 버튼을 생성

### 2-2-2. 주요 속성

-   `type`: 버튼 유형 지정 (submit, reset, button)

### 2-3-3. `<button>` 태그 사용 예시

```html
<!-- 기본값은 submit → 클릭 시 폼 제출 -->
<button type="submit">제출</button>
```

## 2-4. `<select>` & `<option>` 태그

### 2-4-1. `<select>` & `<option>` 태그란?

-   드롭다운 목록 생성
-   `<select>` → 리스트 정의
-   `<option>` → 각 항목 정의

### 2-4-2. 주요 속성

-   `<select name="...">`: 서버에 전송될 키 이름 지정
-   `<option value="...">`: 선택 시 서버로 전달될 값

### 2-4-3. `<select>` & `<option>` 태그 사용 방법

```html
<select name="country">
    <option value="kr">한국</option>
    <option value="us">미국</option>
    <option value="jp">일본</option>
</select>
```

> 💡 활용 팁
>
> -   유효성 검사 속성 → 사용자 경험 향상
> -   `label`, `for` 속성 → 접근성 향상 (스크린 리더 사용자 등 고려)
> -   `autocomplete = "off"` 속성 → 자동 완성 방지
> -   HTTPS & CSRF 방지 토큰 → 안전한 데이터 처리
