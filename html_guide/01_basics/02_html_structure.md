# 2. HTML 요소와 문서 구조

## 2-1. HTML 요소의 구조

### 2-1-1. 기본 구조

```html
<!-- 여는 태그와 닫는 태그로 구성 -->
<태그이름>내용</태그이름>
```

### 2-1-2. 빈 요소

```html
<!-- 내용 없이 단독으로 사용 + 닫는 태그 X -->
<img src="image.jpg" alt="이미지 설명" />
```

### 2-1-3. 주석

```html
<!-- 이 부분은 브라우저에서 표시되지 않습니다 -->
```

## 2-2. HTML 문서의 구조

```html
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <meta name="description" content="HTML 문서의 메타 태그를 설명합니다." />
        <meta name="keywords" content="HTML, Meta, SEO" />
        <title>기본 HTML 구조</title>
    </head>
    <body>
        <h1>제목 태그</h1>
        <p>단락 태그</p>
    </body>
</html>
```

### 2-2-1. 주요 구성 요소

-   `<!DOCTYPE html>`: 브라우저가 최신 HTML 규칙을 적용하여 해석하도록 지시
-   `<lang>`: 문서의 기본 언어 설정 (HTML 문서의 최상위 루트 요소)
-   `<head></head>`: 문서의 메타데이터를 포함하는 영역 (화면에 직접 보이지 않음)
-   `<body></body>`: 웹 페이지의 실제 콘텐츠를 포함하는 영역

### 2-2-2. 주요 메타 태그

-   `<title></title>`: 브라우저 탭, 검색 결과에 표시되는 제목
-   `charset`: 문자 인코딩 설정 (`UTF-8` 추천)
-   `description`: 검색 결과에 표시될 페이지 설명
-   `keywords`: 페이지와 관련된 키워드 (현재 중요도 낮음)
-   `viewport`: 모바일 환경 대응 (반응형 웹디자인 구현 시 필수 설정)

## 2-3. 메타데이터

### 2-3-1. 메타데이터란?

-   웹 페이지의 정보를 설명하는 데이터
-   검색 엔진, 브라우저 등에서 사용
-   문서의 <head> 안에 위치

### 2-3-2. 메타데이터 활용 팁

-   페이지별 고유 메타데이터 설정
-   메타 설명은 150 ~ 160자 이내로 요약
-   모바일 최적화를 위한 `viewport` 설정 권장
