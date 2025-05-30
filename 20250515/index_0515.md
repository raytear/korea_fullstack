# 2025-05-15 수업 정리: body 태그 안의 글자 및 서식 태그

## 📌 `<body>` - 글자 및 서식 태그
- body 태그 내부에 위치하는 **글자 출력 및 서식 지정 태그**들을 학습
- HTML 문서에서 사용자에게 **보이는 정보**를 구성하는 방법 익히기

---

## 🧾 카테고리 분류
1. **글자 및 서식** ✅ 오늘 수업
2. 멀티미디어
3. 입력
4. 기타

---

## 🧩 제목 및 본문 관련 태그

### `<h1>` ~ `<h6>`
- 제목을 출력하는 태그 (숫자가 클수록 글자 크기 작아짐)
```html
<h1>가장 큰 제목</h1>
<h2>소제목</h2>
```

### `<pre>`
- 입력한 텍스트를 **있는 그대로** 화면에 출력 (공백/줄바꿈 유지)
```html
<pre>
이 문장은 줄바꿈과
    들여쓰기가 그대로 보입니다.
</pre>
```

### `<hgroup>`
- 제목과 본문을 하나의 묶음으로 그룹화
```html
<hgroup>
  <h1>제목</h1>
  <pre>본문 내용</pre>
</hgroup>
```

---

## ✨ 서식 태그 정리

| 태그 | 기능 설명 | 예시 |
|------|-----------|------|
| `<strong>` / `<b>` | 글자를 **두껍게** | `<strong>강조</strong>` |
| `<em>` / `<i>`     | 글자를 *기울이기* | `<em>기울임</em>` |
| `<ins>` / `<u>`    | 글자에 **밑줄** | `<ins>밑줄</ins>` |
| `<del>` / `<s>`    | 글자에 ~~취소선~~ | `<del>삭제</del>` |
| `<sup>`            | 윗첨자 | `H<sup>2</sup>O` |
| `<sub>`            | 아랫첨자 | `log<sub>10</sub>` |
| `<ruby>` + `<rt>` + `<rp>` | 일본어 후리가나 표기 | `<ruby>公差<rp>(</rp><rt>コシャ</rt><rp>)</rp></ruby>` |

---

## 📄 일반 본문 출력 태그

### `<p>`
- 일반적인 본문 단락 출력
```html
<p>이것은 일반 문단입니다.</p>
```

---

## 🔀 줄바꿈 태그

### `<br/>`
- 텍스트 중간에서 줄바꿈을 할 때 사용
```html
<p>첫 줄<br/>두 번째 줄</p>
```

---

## 💡 요약
- 모든 디스플레이 태그는 `<body>` 안에서 사용됨
- 서식 태그들을 적절히 조합하여 사용자에게 잘 보이는 문서를 구성할 수 있음