# 2025-05-28 수업 정리: CSS Animation 속성

## ✨ Animation 속성

### 개요

- 기본 디자인에 **생동감을 부여**하여 사용자 경험을 높임
- 핵심 속성: `transition`, `animation`

---

### 1. 간단 Animation: `transition`

```css
/* transition: 속성 변화 시 서서히 변화 적용 */
transition: background-color 1s ease 0s;
transition: width 0.5s linear 0s;
transition: all 0.3s ease-in-out 0s;
```

- 작성법: `transition: 대상 시간 공식 딜레이;`

#### 🕒 시간 단위 예시

- `1s`  ← 1초  
- `0.5s`  ← 0.5초

#### 🧮 공식 예시

- `linear` → 선형: 일정한 속도  
- `ease-in` → 느리게 시작  
- `ease-out` → 느리게 끝남  
- `ease-in-out` → 느림 → 빠름 → 느림  
- `cubic-bezier()` → 사용자 정의 곡선

#### ⏱️ 딜레이

- `0s` → 지연 없음

#### ⚠️ 주의

- **숫자가 아닌 속성**(예: `font-name`)은 서서히 변화할 수 없음

---

### 2. 복잡 Animation: `@keyframes` + `animation`

#### 🧩 `@keyframes`

```css
/* @keyframes: 애니메이션 단계 지정 */
@keyframes move {
  0%   { left: 0px; }
  50%  { left: 250px; }
  100% { left: 0px; }
}
```

#### 🛠️ `animation`

```css
/* animation: keyframes 기반 애니메이션 실행 */
animation: move 3s ease-in-out 0s alternate infinite running;
```

- 작성법: `animation: 이름 시간 공식 딜레이 방향 횟수 상태;`

#### 🔁 방향

- `normal`: 정방향  
- `alternate`: 왕복  
- `reverse`: 역방향  
- `alternate-reverse`: 왕복 역방향 시작

#### 🔂 반복 횟수

- `1`: 한 번만 실행  
- `infinite`: 무한 반복

#### ⏳ 실행 상태

- `running`: 실행 중  
- `paused`: 일시 정지

---

### 3. Animation 예시

#### 🌍 태양계 회전 예시

```html
<img src="https://www.pngarts.com/files/10/Earth-PNG-Image-Transparent-Background.png" alt="지구">
<div>
  <img src="https://www.pngarts.com/files/4/Sun-PNG-Image-Transparent.png" alt="태양">
</div>
```

---

#### 📝 입력창 애니메이션

```html
<div class="input text-type">
  <input type="text">
  <div class="underline def"></div>
  <div class="underline over"></div>
</div>
```

---

#### 🔘 버튼 애니메이션

```html
<button>버튼</button>
```