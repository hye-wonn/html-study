# 1. IFrame과 임베드 요소

## 1-1. Iframe

### 1-1-1. Iframe이란?

-   다른 웹 페이지나 콘텐츠를 **현재 HTML 페이지에 삽입**할 수 있는 요소
-   외부 콘텐츠 (e.g. YouTube, 지도, 다른 HTML 문서) 삽입에 사용

### 1-1-2. 주요 속성

-   `src`: 삽입할 콘텐츠의 URL 지정
-   `width`, `height`: 너비, 높이 (단위: px)
-   `title`: 콘텐츠의 제목 (접근성 향상용)
-   `loading`: 로딩 방식 지정 (`lazy` / `eager`)
-   `allowfullscreen`: 전체 화면 허용
-   `sandbox`: 콘텐츠에 제한을 걸어 보안 강화 (`allow-scripts`, `allow-same-origin`, etc.)

### 1-1-3. Iframe 사용 예시

```html
<iframe
    src="https://www.youtube.com/embed/dQw4w9WgXcQ"
    width="560"
    height="315"
    title="YouTube 영상"
    loading="lazy"
    allowfullscreen
    sandbox="allow-scripts allow-same-origin"
></iframe>
```

> 💡 추가 설명
>
> -   `lazy` → 사용자가 해동 요소를 보기 전까지 로딩 X (성능 최적화)
> -   `eager` → 페이지 로드 시 바로 로딩

> 💡 활용 팁
>
> -   외부 콘텐츠 → 보안을 위해 `sandbox` 속성 사용
> -   SEO 최적화가 필요한 콘텐츠 → IFrame < 직접 삽입 (검색 엔진 직접 접근 X)

## 1-2. 임베드 요소

### 1-2-1. 임베드 요소란?

-   외부 미디어(PDF, 비디오 등)나 앱을 현재 페이지에 삽입할 때 사용
-   `<embed>`: 단순 삽입
-   `<object>`: 고급 설정 가능

### 1-2-2. `<embed>` 태그

-   `src`: 포함할 파일 경로 지정
-   `type`: MIME (미디어) 타입 지정 (e.g. `application/pdf`)
-   `width`, `height`: 콘텐츠 표시 영역 크기 지정

```html
<embed src="example.pdf" type="application/pdf" width="600" height="400" />
```

### 1-2-3. `<object>` 태그

-   `data`: 포함할 파일 경로 지정
-   `type`: MIME (미디어) 타입 지정
-   `width`, `height`: 콘텐츠 표시 영역 지정

```html
<object data="example.pdf" type="application/pdf" width="600" height="400">
    이 브라우저는 PDF를 지원하지 않습니다.
    <a href="example.pdf">PDF 다운로드</a>
</object>
```

> 💡 활용 팁 및 주의 사항
>
> -   `<object>` → 대체 콘텐츠 제공 가능 (사용자 경험 개선)
> -   PDF 등은 `embed`보다 `object`가 호환성이 더 좋음
> -   브라우저 호환성에 차이가 존재함을 유의
