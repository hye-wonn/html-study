# 2. 비디오 태그 (`<video>`)

## 2-1. 비디오 태그란?

-   웹 페이지에 비디오를 사입하는 데 사용
-   다양한 속성을 통해 재생, 일시 정지, 음소거 등의 비디오 제어 기능 제공

## 2-2. 주요 속성

-   `src`: 비디오 파일 경로 지정
-   `controls`: 재생/일시정지 등의 컨트롤러 표시
-   `autoplay`: 자동 재생
-   `muted`: 음소거 상태로 시작
-   `loop`: 반복 재생
-   `poster`: 로딩 전 대체 이미지

## 2-3. 비디오 태그 사용 예시

```html
<!-- 큰 용량으로 압축하거나 낮은 해상도의 파일을 사용하는 것을 권장-->
<video src="video.mp4" width="640" height="360" controls autoplay muted loop></video>
```

> 💡 `<source>` 태그로 여러 포맷 지원 시, 사용자에게 최적화된 형식으로 재생 가능

```html
<!-- 여러 포맷 지원 예시 -->
<video width="640" height="360" controls>
    <source src="movie.mp4" type="video/mp4" />
    <source src="movie.ogg" type="video/ogg" />
    브라우저가 비디오 태그를 지원하지 않습니다.
</video>
```
