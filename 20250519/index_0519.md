# 2025-05-19 수업 정리: 구조화 태그

## 📌 구조화 태그
- HTML 콘텐츠는 기본적으로 **위에서 아래로** 쌓이므로, **좌우 배치가 어려움**
- 구조화 태그는 콘텐츠 자체를 표시하지 않고, **위치와 구역을 나누는 역할**
- 대표 예: 리스트, 정의형 목록, 아코디언, 표 등

---

## 🔢 Ordered List (`<ol>`)  
- **순서 있는 목록**을 구성할 때 사용  
- 숫자/알파벳/로마자 등으로 항목을 자동 번호 매김  

### ✅ 주요 속성
| 속성 | 설명 |
|------|------|
| `type` | 번호 형태 지정 (1, a, A, i, I) |
| `start` | 시작 번호 지정 |
| `reversed` | 역순 나열 |

```html
<ol type="a" start="2" reversed>
  <li>순서 1</li>
  <li>순서 2</li>
  <li>순서 3</li>
</ol>
```

---

## 🔸 Unordered List (`<ul>`)  
- **순서 없는 목록**을 만들 때 사용

### ✅ 주요 속성
| 속성 | 설명 |
|------|------|
| `type` | 아이콘 형태 (disc: ●, circle: ○, square: ■, none) |

```html
<ul type="circle">
  <li>비순차 항목 A</li>
  <li>비순차 항목 B</li>
</ul>
```

---

## 📚 정의형 리스트 (`<dl>`, `<dt>`, `<dd>`)  
- 용어와 정의 쌍을 묶을 때 사용  
- 한 개의 `<dl>` 안에는 보통 **1개의 `<dt>`와 `<dd>`**

```html
<dl>
  <dt>HTML</dt>
  <dd>웹문서를 구성하는 마크업 언어</dd>
</dl>
```

---

## 🔽 Details & Summary (`<details>`, `<summary>`)  
- **아코디언 UI처럼 펼침/접기** 기능 구현  
- `<summary>`는 제목, `<details>`는 본문  

```html
<details>
  <summary>자세히 보기</summary>
  숨겨진 내용을 이곳에 작성할 수 있습니다.
</details>

<details open>
  <summary>항상 열림</summary>
  이 항목은 기본적으로 열려 있습니다.
</details>
```

---

## 📊 Table (`<table>`)  
- HTML에서 **표 구조**를 만들 때 사용

### ✅ 주요 속성
| 속성 | 설명 |
|------|------|
| `border` | 테두리 두께 |
| `cellspacing` | 셀 간 간격 |
| `cellpadding` | 셀 내부 여백 |

### ✅ 표 구성 태그
| 태그 | 설명 |
|------|------|
| `<thead>` | 표의 머리말 영역 |
| `<tbody>` | 실제 내용 |
| `<tfoot>` | 요약 또는 꼬리말 |
| `<tr>` | 표의 한 줄 |
| `<th>` | 제목 셀 (굵게/가운데) |
| `<td>` | 일반 데이터 셀 |

```html
<table border="2" cellspacing="4" cellpadding="8">
  <thead>
    <tr>
      <th rowspan="2" align="center">이름</th>
      <th colspan="2" align="center">연락처</th>
    </tr>
    <tr>
      <th>이메일</th>
      <th>전화번호</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>홍길동</td>
      <td>hong@example.com</td>
      <td>010-1234-5678</td>
    </tr>
    <tr>
      <td>이몽룡</td>
      <td>lee@example.com</td>
      <td>010-4321-8765</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="3" align="right">총 2명</td>
    </tr>
  </tfoot>
</table>
```

---

## ✅ 요약
- 구조화 태그는 **정보의 내용을 분리하거나 구획화**하는 데 사용
- 목록, 정의, 표 등은 사용자 경험을 크게 향상시킴
