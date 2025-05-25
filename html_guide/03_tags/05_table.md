# 1. 표 태그

## 1-1. 주요 태그

-   `<table>`: 표 전체 구조 정의
-   `<caption>`: 표 제목 정의
-   `<thead>`: 머리 부분 (보통 `<th>` 포함)
-   `<tbody>`: 본문 내용
-   `<tfoot>`: 표의 하단 요약
-   `<tr>`: 행(row) 정의
-   `<th>`: 헤더 셀 (굵고 중앙 정렬)
-   `<td>`: 데이터 셀 (일반 셀)

## 1-2. 표 태그 사용 예시

```html
<table>
    <caption>
        참가 명단
    </caption>
    <thead>
        <tr>
            <th>이름</th>
            <th>나이</th>
            <th>전화번호</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>참가자1</td>
            <td>20</td>
            <td>010-xxxx-xxxx</td>
        </tr>
        <tr>
            <td>참가자2</td>
            <td>21</td>
            <td>010-nnnn-nnnn</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="3">총 2명</td>
        </tr>
    </tfoot>
</table>
```

> 💡 활용 팁
>
> -   `<caption>`, `<th scope = "col">`, etc. → 접근성 향상
> -   CSS → 가독성 개선
