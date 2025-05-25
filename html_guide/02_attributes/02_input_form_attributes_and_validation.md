# 2. 입력 폼과 유효성 검사

## 2-1. 입력 폼 주요 속성

### 2-1-1. `type`

-   입력 필드의 타입 설정 (text, email, password 등)
-   사용자가 입력한 값이 설정한 타입인지 자동 검사

```html
<input type="email" placeholder="이메일 입력" />
```

### 2-1-2. `value`

-   초기 표시 값 설정

```html
<input type="text" value="기본값" />
```

### 2-1-3. `placeholder`

-   입력 전 안내 힌트 표시

```html
<input type="text" placeholder="이름 입력" />
```

### 2-1-4. `disabled`

-   입력 불가 상태

```html
<input type="text" disabled />
```

## 2-2. 유효성 검사

### 2-2-1. 필수 입력 (`required`)

```html
<input type="email" name="email" required />
```

### 2-2-2. 입력 패턴 검사 (`pattern`)

```html
<input type="text" name="username" pattern="[A-Za-z]{3,}" title="영문자 3자 이상 입력하세요." />
```

### 2-2-3. 숫자 및 날짜 최대/최솟값 설정 (`min` / `max`)

```html
<input type="number" min="1" max="100" />
```

### 2-2-4. 최대/최소 문자 수 제한 (`minlength` / `maxlength`)

```html
<input type="text" name="id" minlength="5" maxlength="10" />
```

### 2-2-5. 형식 검사 (`type`)

-   `email`, `tel`, `url`, `number`, `date`, `time`, `color` 등

```html
<input type="email" name="email" />
<input type="tel" name="phone" />
<input type="url" name="homepage" />
```
