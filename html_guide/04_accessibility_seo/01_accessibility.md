# 1. 접근성 (Accessibility)

## 1-1. 접근성 개요

-   장애가 있는 사용자도 웹을 사용할 수 있도록 돕는 기술과 설계 방식

## 1-2. ARIA (Accessible Rich Internet Applications) 속성

### 1-2-1. ARIA 속성이란?

-   스크린 리더가 웹 페이지의 구조와 기능을 더 잘 이해하도록 도움
-   동적 콘텐츠나 사용자 상호작용이 많은 웹 애플리케이션에서 유용

### 1-2-2. 주요 속성

-   `aria-label`: 요소의 기능 설명 (화면에 보이지 않아도 스크린 리더가 읽음)
-   `role`: 요소의 역할 명시 (예: `button`, `dialog`)

### 1-2-3. ARIA 속성 사용 예시

```html
<button aria-label="메뉴 열기">≡</button>
```

## 1-3. 대체 텍스트 (`alt`)

-   이미지 로드 X / 스크린 리더 사용자 → 이미지 설명 제공

```html
<img src="logo.png" alt="로고 설명" />
```

## 1-4. 입력 필드와 레이블 연결

-   레이블 태그를 통해 설명 추가

```html
<label for="username">사용자 이름</label> <input type="text" id="username" name="username" />
```

## 1-5. 키보드 네비게이션

-   키보드만 모든 요소 접근 가능

```html
<!-- tabindex: 키보드 포커스 순서 지정 -->
<button tabindex="0">확인</button>
```

> 💡 활용 팁 및 주의 사항
>
> -   의미 없는 ARIA 남용 금지
> -   자동 포커스 피하기 (사용자 제어권 보장)
