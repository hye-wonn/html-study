# 1. 글로벌 속성

## 1-1. `class`

-   CSS, JavaScript 이벤트를 적용할 대상 지정
-   여러 클래스를 공백으로 구분해 동시 적용 가능

```html
<!-- 굵은 글씨 + 노란 배경 -->
<p class="bold highlight">텍스트</p>
```

```css
.bold {
    font-weight: bold;
}

.highlight {
    background-color: yellow;
}
```

## 1-2. `id`

-   요소에 고유 식별자 부여
-   JS → 요소 조작, CSS → `#id명`으로 스타일 지정

```html
<!-- 하나의 HTML 문서 안에서 중복되면 안됨 -->
<button id="submit_button">버튼</button>
```

```css
/* `#id명`으로 스타일 지정 */
#submit_button {
    background-color: blue;
    color: white;
}
```

```js
// 요소 조작
document.getElementById('submit_button').addEventListener('click', () => {
    alert('버튼이 클릭됨!');
});
```

## 1-3. `style`

-   요소에 직접 인라인 스타일 지정 (유지보수 → 외부 CSS 사용 권장)

```html
<p style="color: red;">텍스트</p>
```

## 1-4. `lang`

-   요소의 언어 설정
-   스크린 리더, 검색 엔진에 언어 정보 제공

```html
<p lang="ko">한국어 텍스트</p>
```

> 💡 스크린 리더: 시각장애인 등 시각적 접근이 어려운 사용자를 위해 화면의 내용을 음성으로 읽어주는 보조 기술

## 1-5. `title`

```html
<!-- 마우스 오버 시 "버튼 클릭하기!"라는 툴팁 표시 -->
<button title="버튼 클릭하기!"></button>
```

> 💡 스크린 리더에 잘 읽히지 않을 수도 있으므로 시각 장애인을 고려한다면 `aria-label` 사용을 고려

## 1-6. `hidden`

-   화면에서 요소 숨기기

```html
<div hidden>텍스트</div>
```

## 1-7. `dir`

-   텍스트 방향 설정 (ltr / rtl)

```html
<p dir="rtl">텍스트</p>
```

## 1-8. `accesskey`

-   단축키 지정

```html
<button accesskey="s">저장 버튼</button>
```

> 💡 브라우저/OS마다 단축키 조합이 달라 접근성 혼란을 초래 → 시각적으로 단축키 정보를 함께 표시 권장

## 1-9. `draggable`

-   요소를 드래그할 수 있게 설정

```html
<img src="image.png" draggable="true" alt="드래그 가능한 이미지" />
```

## 1-10. `spellcheck`

-   맞춤법 검사 기능 설정 (`true` / `false`)

```html
<textarea spellcheck="true">맞춤법 검사 텍스트</textarea>
```

## 1-11. `contenteditable`

-   사용자가 직접 내용 편집 가능하게 설정

```html
<div contenteditable="true">편집 가능 텍스트</div>
```

## 1-12. `tabindex`

-   키보드 `Tab` 키로 요소 간 포커스 이동 순서 지정
-   너무 많은 요소에 수동으로 지정 시 접근성 혼란 초래

```html
<!-- 로그인 시 Tab 키로 아이디 → 비밀번호 → 로그인 버튼 순으로 이동 -->
<input type="text" tabindex="1" />
<input type="password" tabindex="2" />
<button tabindex="3">로그인</button>
```

> 💡 대부분의 경우 tabindex="0" 또는 tabindex="-1" 정도만 필요하며, 양수 값은 정말 필요한 경우에만 사용하는 것을 권장

## 1-13. `translate`

-   자동 번역 여부 설정 (`yes` / `no`)

```html
<p translate="no">번역하지 않을 텍스트</p>
```

## 1-14. `data-*`

-   JS용 사용자 정의 데이터 저장
-   `element.dataset.user` 등으로 접근

```html
<div data-user="12345">사용자 정보</div>
```

## 1-15. `autofocus`

-   페이지 로드 시 자동 포커스 설정

```html
<!-- 페이지를 열자마자 커서가 깜빡거림 -->
<input type="text" autofocus />
```
