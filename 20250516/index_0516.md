# 2025-05-16 수업 정리: HTML 멀티미디어 태그

## 📌 멀티미디어 태그
- HTML에서 **이미지, 비디오, 오디오, 외부 콘텐츠**를 웹페이지에 삽입하는 방법

---

## 🧾 카테고리 분류
1. 글자 및 서식
2. **멀티미디어** ✅ 오늘 수업
3. 입력
4. 기타

---

## 🖼️ 이미지 태그

### `<img>`
- 웹페이지에 이미지를 삽입
- 태그만으로는 이미지 경로가 없으므로 `src` 속성 필수
- 주요 속성:

| 속성 | 설명 | 예시 |
|------|------|------|
| `src` | 이미지 경로 지정 | `/apple.jpg`, `./img.jpg`, `https://...` |
| `alt` | 이미지가 로딩되지 않을 때 대체 텍스트 | `<img src="x.jpg" alt="이미지 없음" />` |
| `loading` | 이미지 로딩 시점 설정 (eager / lazy) | `<img loading="lazy" />` |
| `width`, `height` | 크기 지정 | `<img width="100px" height="100px" />` |

### `<figure>` + `<figcaption>`
- 이미지와 그에 대한 설명을 묶는 구조
```html
<figure>
  <img src="apple.jpg" alt="사과" />
  <figcaption>사과 사진</figcaption>
</figure>
```

### `<svg>`
- 해상도 손실 없이 그림을 표현하는 벡터 기반 이미지
- 일러스트, 로고 등에서 사용
```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" fill="yellow" />
</svg>
```

### `<picture>` + `<source>` + `<img>`
- 화면 크기 또는 조건(media)에 따라 **다른 이미지를 선택해서 불러옴** (교체 로딩)
- 마지막에는 `<img>` 태그가 반드시 포함되어야 함
```html
<picture>
  <source srcset="large.jpg" media="(min-width:800px)" />
  <source srcset="small.jpg" media="(max-width:799px)" />
  <img src="fallback.jpg" alt="기본 이미지" />
</picture>
```

#### 💡 교체 로딩
> 조건(media query 등)에 따라 준비해둔 여러 이미지 중 **가장 알맞은 이미지를 선택해 로딩**
> 사용자의 **화면 크기나 환경에 따라 이미지가 자동으로 바뀜**

---

## 🎬 비디오 태그

### `<video>`
- 비디오 파일 삽입
- 주요 속성:

| 속성 | 설명 |
|------|------|
| `src` | 비디오 경로 |
| `controls` | 재생/일시정지 등 컨트롤러 표시 |
| `autoplay` | 자동 재생 (정책상의 이유로 사운드 포함시 자동 실행 불가) |
| `muted` | 음소거 상태로 재생 |

- 여러 포맷을 지원하려면 `<source>` 태그를 내부에 사용
```html
<video width="320" height="240" controls>
  <source src="video.mp4" type="video/mp4" />
  <source src="video.webm" type="video/webm" />
</video>
```

---

## 🎧 오디오 태그

### `<audio>`
- 오디오 파일 삽입 (video와 구조 거의 동일)
```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg" />
  <source src="audio.ogg" type="audio/ogg" />
</audio>
```

---

## 🌐 외부 콘텐츠 삽입

### `<iframe>`
- 외부 웹페이지를 현재 웹페이지 안에 삽입
- 주로 지도, 다른 사이트 포함, 유튜브 등에서 활용
```html
<iframe src="https://www.inven.co.kr/" width="600" height="400"></iframe>
```

---

## 💡 요약
- 멀티미디어 태그는 시각/청각 자료를 웹페이지에 직접 포함할 수 있게 해줌
- `<img>`, `<video>`, `<audio>`는 각각 `src`를 통해 소스를 불러옴
- `<picture>` 및 `<source>`는 조건에 따라 미디어를 교체 로딩
- `<iframe>`은 외부 웹페이지 전체를 내장 가능