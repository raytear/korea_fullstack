# 2025-05-30 수업 정리: CSS 고급 기능

## 🔧 CSS 확장 기능: 변수, 덮어쓰기, 반응형 등

---

### 🎨 CSS 변수

```css
:root {
  --brand-color: hsl(182, 83%, 43%);
}

h1 {
  color: var(--brand-color);
}
```

- `--brand-color`: 전역에서 사용 가능한 변수
- `var(--brand-color)`: 해당 변수를 불러와 적용

---

### ⚠️ 덮어쓰기

#### ✅ `!important`

```css
h1 {
  color: red !important;
}
```

- 우선순위를 무시하고 **강제로 스타일 적용**

#### ✅ `@layer`

```css
@layer base, theme, component;

@layer base {
  h1 { color: red; }
}
@layer component {
  h1 { color: blue; }
}
```

- CSS **렌더링 우선순위**를 명시적으로 조절하는 방법

---

### 📱 반응형 웹: Media Query

```css
@media screen and (max-width: 600px) {
  h1 {
    font-size: 1.2rem;
  }
}
```

- 화면 너비가 600px 이하일 때만 적용
- 모바일 환경 등에 적절한 스타일 분기 가능

---

### 📦 Container Query

```css
div {
  container-type: inline-size;
  container-name: exampleContainer;
}

@container exampleContainer (min-width: 500px) {
  h1 {
    color: green;
  }
}
```

- **해당 요소 내부 너비**가 500px 이상일 때만 스타일 적용
- 부모 요소 크기에 따라 스타일 제어 가능

---

### 📐 컨테이너 단위

- `cqw`: container width의 1%
- `cqh`: container height의 1%
- `cqmin`: width, height 중 작은 쪽의 1%
- `cqmax`: width, height 중 큰 쪽의 1%

---

### 🧪 예시 HTML

```html
<div>
  <h1>Hello</h1>
  <h2>Hello</h2>
</div>
<h1>Hello</h1>
```

- Container Query나 Media Query 실습 시 사용하는 기본 구조