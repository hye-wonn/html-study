# 3. 오디오 태그 (`<audio>`)

## 3-1. 오디오 태그란?

-   웹 페이지에 오디오를 삽입하는 데 사용
-   재생, 일시 정지, 볼륨 조절 등의 제어 기능 제공

## 3-2. 주요 속성

-   `src`: 오디오 파일 경로 지정 (`<source>` 태그 → 다양한 형식을 지원)
-   `controls`: 재생, 일시 정지, 볼륨 조절 등의 기본 컨트롤 제공
-   `autoplay`: 자동 재생
-   `loop`: 반복 재생
-   `muted`: 음소거 상태로 시작

## 3-3. 오디오 태그 사용 예시

```html
<!-- 큰 오디오 파일은 압축하거나 스트리밍 형식으로 제공하는 것을 권장 -->
<audio src="sound.mp3" controls autoplay muted loop></audio>
```

> 💡 `<source>` 태그로 여러 포맷 지원 시, 사용자에게 최적화된 형식으로 재생 가능

```html
<!-- 여러 포맷 지원 예시 -->
<audio controls>
    <source src="audio.mp3" type="audio/mpeg" />
    <source src="audio.ogg" type="audio/ogg" />
    브라우저가 오디오 태그를 지원하지 않습니다.
</audio>
```
