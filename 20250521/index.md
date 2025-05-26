
# 2025-05-21 수업 정리: HTML Request 태그

## 📮 `<form>` - 서버에 정보 요청

- 입력 데이터를 서버로 전달할 때 사용
- 내부의 `<input>`, `<select>`, `<textarea>` 등의 값을 함께 전송

### ✅ 주요 속성

| 속성명    | 설명 |
|-----------|------|
| `action`  | 데이터를 보낼 대상 주소 |
| `method`  | 데이터를 전송하는 방식 (GET / POST) |
| `enctype` | 데이터 인코딩 방식 (텍스트, 파일 등) |

---

### 📌 `action` 예시

- `https://www.naver.com/path/to` → 다른 서버로 요청  
- `/path/to` → 현재 서버로 요청  

---

### 📌 `method` 종류

- **GET**: 주소에 데이터를 포함 (예: `?a=b&c=d`)  
- **POST**: 데이터를 Body 내부에 포함 (주소에 노출되지 않음)

---

### 📌 `enctype` 종류

| enctype                         | 설명                        |
|----------------------------------|-----------------------------|
| `application/x-www-form-urlencoded` | 기본값, 텍스트 데이터 전송 |
| `multipart/form-data`               | 파일 데이터 전송에 사용     |

---

### 🧪 예제 1: 로그인 폼 (GET 방식)

```html
<form action="https://www.naver.com/path/to">
  <input name="id" type="text" placeholder="아이디"/>
  <input name="pw" type="password" placeholder="비밀번호"/>
  <button type="submit">로그인</button>
</form>
```

---

### 🧪 예제 2: 검색 폼 (GET + fieldset)

```html
<form action="https://search.naver.com/search.naver" method="get">
  <input name="where" value="nexearch" type="hidden"/>
  <input name="sm" value="top_sug.pre" type="hidden"/>
  <input name="fbm" value="0" type="hidden"/>
  <input name="acr" value="1" type="hidden"/>
  <input name="qdt" value="0" type="hidden"/>
  <input name="ie" value="utf8" type="hidden"/>
  <input name="ackey" value="gs54pjbq" type="hidden"/>

  <fieldset>
    <legend>검색어</legend>
    <input name="query" type="text" placeholder="검색어 입력"/>
  </fieldset>
  <button type="submit">검색</button>
</form>
```

---

### 🧪 예제 3: 파일 업로드 (POST + multipart/form-data)

```html
<form action="https://redd.it/new.json/" method="post" enctype="multipart/form-data">
  <input type="file" name="uploadFile"/>
  <button type="submit">업로드</button>
</form>
```

---

## 🖲️ `<button>` - 클릭 가능한 버튼

- `<input type="submit">`과 유사하지만 더 유연한 버튼 사용 가능

### ✅ 주요 type

| type       | 설명            |
|------------|-----------------|
| `submit`   | 폼 데이터 제출  |
| `reset`    | 입력 초기화     |
| `button`   | 일반 버튼 (JS)  |

```html
<button type="submit">제출</button>
<button type="reset">초기화</button>
<button type="button">버튼</button>
```

---

## 🧱 `<fieldset>` / `<legend>` - 입력 그룹화

- `<fieldset>`: 입력 요소 그룹에 외곽선
- `<legend>`: 해당 그룹의 제목 지정

```html
<fieldset>
  <legend>회원가입</legend>
  <input type="text" name="username"/>
  <input type="password" name="pw"/>
</fieldset>
```

---

## ✅ 요약

- `form`은 데이터를 서버로 전달할 수 있는 가장 핵심적인 태그
- `method`, `enctype` 속성 조합에 따라 전달 방식과 데이터 종류가 달라짐
- 버튼과 입력 필드, 그룹화 태그를 적절히 조합하여 UI를 구성할 것
