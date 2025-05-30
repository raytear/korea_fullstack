# 2025-05-29 수업 정리: Flex & Grid

## 📦 레이아웃 속성 개요

- 애니메이션이나 반응형 UI를 만들 때 **태그 위치 제어**가 중요
- 이를 위해 `position`, `top`, `left` 외에도 **`flex`, `grid`** 속성을 활용

---

## 🔹 Flex 예시

> 유연한 1차원 배치를 위한 속성

```css
/* .row: Flex container 설정 */
.row {
  width: 150px;
  height: 150px;
  background-color: greenyellow;
  display: flex;         /* flex 레이아웃 지정 */
  flex-direction: row;   /* 주 축 방향: 가로 */
  flex-wrap: nowrap;     /* 넘침 방지 없음 */
}

/* .item: Flex item 설정 */
.item {
  border: 1px black solid;
  /* flex-grow: 1; */
  /* flex-shrink: 0; */
}
```

### ✅ Flex 주요 속성

- `display: flex` → 부모를 Flex container로 설정  
- `flex-direction: row` → 아이템 가로 배치  
- `flex-wrap: nowrap` → 줄바꿈 없음  
- `justify-content: center` → 주축 기준 중앙 정렬  
- `align-items: center` → 교차축 기준 중앙 정렬

---

## 🔹 Grid 예시

> 2차원 격자 배치를 위한 속성

```css
/* .container: Grid container 설정 */
.container {
  width: 50vw;
  height: 150px;
  background-color: yellow;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
}

/* .id_01: span을 활용한 행 확장 */
.id_01 {
  grid-row-end: span 3;
}
```

### ✅ Grid 주요 속성

- `display: grid` → Grid container 지정  
- `grid-template-columns: repeat(auto-fill, minmax(150px, 1fr))`  
  → 열 자동 채움 + 최소 크기 지정  
- `grid-row-end: span 3` → 해당 항목을 3행(span) 차지하게 설정

---

## 🧪 실습 예시

### 📐 Flex 레이아웃

```html
<div class="row">
  <div class="item id_01">1</div>
  <div class="item id_02">2</div>
  <div class="item id_03">3</div>
  <div class="item id_04">4</div>
  <div class="item id_05">5</div>
  <div class="item id_06">6</div>
  <div class="item id_07">7</div>
  <div class="item id_08">8</div>
  <div class="item id_09">9</div>
</div>
```

### 📐 Grid 레이아웃

```html
<div class="container">
  <div class="item id_01">1</div>
  <div class="item id_02">2</div>
  <div class="item id_03">3</div>
  <div class="item id_04">4</div>
  <div class="item id_05">5</div>
  <div class="item id_06">6</div>
  <div class="item id_07">7</div>
  <div class="item id_08">8</div>
  <div class="item id_09">9</div>
</div>
```

---

## ⚡ 추가: Emmet 문법

> HTML 구조를 빠르게 생성할 수 있는 단축 코드

```emmet
div.container>div.item.id_${$}*9
```

### 💡 해석

- `div.container`: class가 container인 div 생성  
- `>`: 자식 요소 연결  
- `div.item.id_${$}`: item 클래스 + id_01~id_09 자동 생성  
- `*9`: 9번 반복

✅ 입력 후 `Tab` 누르면 자동 완성됨!