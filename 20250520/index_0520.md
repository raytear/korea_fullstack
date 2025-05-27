# 2025-05-20 수업 정리: HTML Interaction 태그

## 📌 Interaction 태그
- 단순 정보 제공을 넘어서, **사용자와의 상호작용**을 가능하게 하는 HTML 태그들
- 입력, 버튼, 선택, 링크 등 사용자 입력 기반 요소 포함

---

## 🔗 `<a>` - 하이퍼링크 태그

```html
<a href="https://www.naver.com" target="_blank">네이버 새 탭 열기</a>
```

---

## 🧾 `<input>` - 다양한 입력 필드

### ✅ 기본 입력 종류

| type           | 설명                        |
|----------------|-----------------------------|
| `text`         | 일반 텍스트 입력            |
| `password`     | 비밀번호 입력 (숨김 처리)    |
| `color`        | 색상 선택                   |
| `file`         | 파일 업로드                 |
| `checkbox`     | 다중 선택                   |
| `radio`        | 단일 선택                   |
| `number`       | 숫자 입력                   |
| `button`       | 일반 버튼                   |
| `reset`        | 입력 초기화 버튼            |
| `submit`       | 입력 제출 버튼              |

```html
<input type="text" placeholder="아이디 입력"/>
<input type="password" placeholder="비밀번호"/>
<input type="color"/>
<input type="number" value="10"/>
<input type="button" value="클릭"/>
<input type="reset"/>
<input type="submit"/>
<input type="file"/>
```

---

### 📅 날짜 및 시간 관련 입력

| type              | 설명                             |
|-------------------|----------------------------------|
| `date`            | 날짜 (년/월/일) 선택             |
| `datetime`        | 전체 날짜 + 시간 (구버전)        |
| `datetime-local`  | 현지 날짜 + 시간 선택            |
| `month`           | 연/월 선택                       |
| `time`            | 시간 선택                        |
| `week`            | 연/주 선택                       |

```html
<input type="date"/>
<input type="datetime"/>
<input type="datetime-local"/>
<input type="month"/>
<input type="time"/>
<input type="week"/>
```

---

## 🏷️ `<label>` - 입력 항목과 연결된 텍스트

```html
<input type="checkbox" id="agree"/>
<label for="agree">약관에 동의합니다</label>
```

---

## 📝 `<textarea>` - 여러 줄 입력창

```html
<textarea rows="4" cols="30">여러 줄의 텍스트를 입력하세요.</textarea>
```

---

## 🔽 `<select>` - 드롭다운 선택

```html
<select name="fruits">
  <option value="apple" selected>사과</option>
  <option value="banana">바나나</option>
  <option value="orange">오렌지</option>
</select>
```

---

## 📁 `<optgroup>` - 드롭다운 항목 그룹화

```html
<select name="food">
  <optgroup label="과일">
    <option>사과</option>
    <option>포도</option>
  </optgroup>
  <optgroup label="야채">
    <option>상추</option>
    <option>오이</option>
  </optgroup>
</select>
```

---

## 🔍 `<datalist>` - 자동완성 드롭다운

```html
<input list="langs" name="language" placeholder="언어 입력"/>
<datalist id="langs">
  <option value="HTML"></option>
  <option value="CSS"></option>
  <option value="JavaScript"></option>
</datalist>
```

---

## ✅ 요약
- `input`, `select`, `label`, `textarea`, `datalist` 등은 사용자와 상호작용을 위한 필수 요소
- 입력 타입이 다양하므로 목적에 맞게 적절히 활용할 것
