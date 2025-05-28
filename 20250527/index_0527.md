# 2025-05-27 수업 정리: CSS 레이아웃 관련 속성

## 🧱 레이아웃 관련 속성

> 텍스트를 넘어서 **영역, 이미지, 위치, 가시성** 등을 제어하기 위한 CSS 속성들

---

### ✅ `width`, `height` - 크기 설정

- 태그의 가로/세로 크기 지정  
- 작성법: `width: 크기; height: 크기;`
- `span`: inline 요소라 크기 적용 안 됨  
- `div`: block 요소로 영역 확보 가능

---

### ✅ `display` - 영역 방식

- 값: `inline`, `block`, `inline-block`, `none`
- `inline-block`: 문자 간 공백 발생 주의

---

### ✅ `padding`, `margin` - 여백 설정

- `padding`: 내부 여백  
- `margin`: 외부 여백  
- 방향 지정 가능: `padding-left`, `margin-top` 등  
- `margin: auto`: 좌우 자동 여백 → 가운데 정렬

---

### ✅ `border`, `outline` - 테두리

- 작성법: `border: 종류 두께 색상;`
- 종류 예시: `solid`, `dashed` 등  
- `none`으로 제거 가능

---

### ✅ `box-sizing` - 크기 계산 기준

| 값            | 설명                           |
|---------------|--------------------------------|
| `content-box` | padding은 크기 외로 계산 (기본값) |
| `border-box`  | padding, border 포함 크기 계산 |

---

### ✅ `background-color` - 배경색 설정

---

### ✅ `background-image` - 배경 이미지/그라디언트

- 사용법: `url('경로')`  
- 또는 `linear-gradient`, `radial-gradient` 등

---

### ✅ `background-size` - 배경 이미지 크기

- `cover`: 큰 축 기준 맞춤  
- `contain`: 작은 축 기준 맞춤

---

### ✅ `border-radius` - 테두리 둥글기

---

### ✅ `overflow` - 넘친 콘텐츠 처리

- 값: `visible`, `hidden`, `scroll`

---

### ✅ `object-fit` - 이미지/비디오 비율 조정

- 값: `cover`, `contain`, `fill`, `none`, `scale-down`

---

### ✅ `left`, `right`, `top`, `bottom` - 위치 이동

- 기준선으로부터 반대 방향으로 이동  
- 예: `left: 50px` → 왼쪽 기준선에서 오른쪽으로 50px 이동

---

### ✅ `position` - 위치 기준 설정

| 값         | 설명                       |
|------------|----------------------------|
| `static`   | 기본 위치                  |
| `relative` | 현재 위치 기준             |
| `absolute` | 상위 요소 기준             |
| `fixed`    | 브라우저 화면 기준         |
| `sticky`   | 특정 위치 도달 시 고정됨   |

---

### ✅ `visibility`, `opacity`, `z-index` - 가시성 설정

- `visibility`: `visible`, `hidden`  
- `opacity`: `0.0 ~ 1.0` (투명도)  
- `z-index`: 요소의 쌓임 우선순위 (높을수록 위)

---

### ✅ `transform` - 요소 변형

- 사용 예시:  
  - `rotate(30deg)`
  - `translate(10px, 20px)`
  - `scale(1.2)`
  - `perspective(300px)`

---

### ✅ `float` - 좌/우 띄우기

- 값: `left`, `right`

---

### ✅ `clear` - float 해제

- 값: `left`, `right`, `both`

---

### ✅ `cursor` - 마우스 커서 모양 설정

---

### ✅ `user-select` - 텍스트 선택 가능 여부

---

### ✅ `box-shadow`, `text-shadow` - 그림자 효과

- 예시: `box-shadow: 2px 2px 5px gray;`

---

### ✅ `filter` - 이미지 효과

- 예시: `blur`, `grayscale`, `sepia`, `contrast` 등

---