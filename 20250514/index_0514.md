# 2025-05-14 수업 정리: head 태그 내부 구성 요소

## 📌 HTML - `<head>`
- HTML의 head 영역에 들어가는 태그들의 이해 및 활용

---

## 📌 `<head>` 태그란?
- 웹페이지의 **구성 정보를 담는 공간**
- `<body>`는 사용자에게 보이는 화면
  `<head>`는 웹페이지의 제목, 설명, 인코딩 등 **보이지 않는 설정 정보**를 담음

---

## 📝 주요 태그 정리

### 1. `<title>`
- **페이지 제목**을 지정하는 태그
- 브라우저 탭에 표시됨
```html
<title>페이지 제목</title>
```

---

### 2. `<meta>`
- 페이지의 메타데이터(정보)를 설정하는 태그
- 동작은 없고, **속성으로 의미를 가짐**

#### 주요 속성

| 속성              | 설명                                   | 예시 |
|-------------------|----------------------------------------|------|
| charset           | 문자 인코딩 지정                        | `<meta charset="UTF-8" />` |
| name="description"| 페이지 설명                            | `<meta name="description" content="이 페이지는..."/>` |
| name="author"     | 작성자 정보                            | `<meta name="author" content="홍길동" />` |
| name="copyright"  | 저작권 정보                            | `<meta name="copyright" content="MyCompany" />` |
| name="robots"     | 검색엔진 크롤링 허용 여부             | `<meta name="robots" content="index, follow" />` |
| name="keywords"   | 검색 키워드                            | `<meta name="keywords" content="html, meta, tag" />` |
| name="revisit-after"| 검색엔진 재방문 주기               | `<meta name="revisit-after" content="7 days" />` |
| name="rating"     | 연령 제한 설정 (general / mature 등) | `<meta name="rating" content="general" />` |

---

### 3. `<link>`
- 외부 파일(CSS, 아이콘 등)을 연결할 때 사용
```html
<link rel="icon shortcut" href="favicon.ico" />
<link rel="stylesheet" href="style.css" />
```

---

## 🌐 소셜미디어 미리보기 설정 태그

### 🔹 Open Graph (`og:`)
- Facebook, Kakao 등에서 링크 미리보기 카드로 보이게 설정
```html
<meta property="og:title" content="페이지 제목" />
<meta property="og:description" content="설명 내용" />
<meta property="og:image" content="image.png" />
<meta property="og:url" content="https://example.com" />
```

### 🔹 Twitter Card (`twitter:`)
- Twitter에서 링크 공유 시 카드로 보이게 설정
```html
<meta name="twitter:title" content="페이지 제목" />
<meta name="twitter:description" content="설명 내용" />
<meta name="twitter:image" content="image.png" />
<meta name="twitter:url" content="https://example.com" />
<meta name="twitter:card" content="summary_large_image" />
```

---

## 💡 요약
- `<head>` 안에는 사용자에게 직접 보이지 않는 페이지 설정 정보들이 들어감
- `<title>`, `<meta>`, `<link>` 태그를 통해 브라우저와 검색엔진, SNS가 이 페이지를 이해할 수 있도록 구성