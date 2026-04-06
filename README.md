# 🐰 NewJeans — Official Fan Archive

> 뉴진스를 사랑하는 팬이 직접 만든 비공식 팬 아카이브 사이트입니다.  
> An unofficial fan archive site crafted with love by a Bunnie.

---
아래 링크로 바로 접속해서 사용할 수 있어요. 아무것도 설치 안 해도 됩니다.

```
https://bigad2007.github.io/New-Jeans/
```

## ⚠️ 중요 고지 / Important Notice

이 프로젝트는 **순수한 팬심으로 제작된 비영리 팬 아카이브**입니다.

- 상업적 이용, 재배포, 무단 도용을 **엄격히 금지**합니다.
- 이 사이트는 ADOR, HYBE 및 관련 권리자와 **일체 관련이 없습니다.**
- 모든 음악, 이미지, 영상의 저작권은 **ADOR · HYBE · 뉴진스** 및 각 권리자에게 있습니다.
- This is a **non-commercial fan project**. All rights to music, images, and videos belong to ADOR, HYBE, and respective rights holders.

> **만약 이 프로젝트를 Fork하거나 참고할 경우, 반드시 동일한 팬 목적으로만 사용해주세요.**  
> If you fork or reference this project, please use it solely for fan purposes with proper attribution.

---

## 📌 프로젝트 소개

| 항목 | 내용 |
|------|------|
| 사이트명 | NewJeans — Official Fan Archive |
| 제작 목적 | 순수 팬 목적의 비공식 아카이브 |
| 대상 그룹 | NewJeans (뉴진스) — 민지, 하니, 다니엘, 해린, 혜인 |
| 소속사 | ADOR · HYBE |
| 데뷔 | 2022년 |

---

## ✨ 주요 기능

### 🖼 갤러리 (Gallery)
- 뉴진스의 공연, 컨셉 아트, 스튜디오 세션 등 다양한 사진 모음
- 호버 시 캡션 표시 및 줌인 효과

### 🎬 뮤직비디오 (Music Videos)
- Attention, Hype Boy, Ditto, OMG, Super Shy, How Sweet 등 주요 MV 임베드
- 유튜브 팝업 플레이어 지원

### 👥 멤버 소개 (Members)
- 민지, 하니, 다니엘, 해린, 혜인 — 5인 멤버 상세 프로필
- 생년월일, 포지션, 소개글 포함

### 💿 음악 (Discography)
- EP, 싱글, 스페셜 앨범 카드형 목록
- 앨범별 수록곡 확인 가능

### 📅 역사 (Timeline)
- 2022년 데뷔부터 현재까지의 주요 활동 타임라인

### 🎤 공연 (Concerts)
- 월드투어, 단독 콘서트 등 공연 기록

### 📝 방명록 (Guestbook)
- 팬들이 익명으로 메시지를 남길 수 있는 공간
- 1시간 쿨다운 제한으로 도배 방지
- 로컬 스토리지 기반 저장

### 🎵 미니 플레이어 (Music Player)
- 하단 고정 플레이어 (Attention, Hype Boy, Ditto 등 16곡)
- 재생/정지, 이전/다음곡, 볼륨 조절, 진행바 클릭 이동 지원
- ⚠️ UI 전용 플레이어입니다. 실제 음원 재생은 지원하지 않으며, 저작권 관계로 음원 파일을 포함하지 않습니다.

---

## 🛠 기술 스택

```
HTML5 · CSS3 · Vanilla JavaScript
```

| 사용 기술 | 설명 |
|-----------|------|
| `Playfair Display` | 세리프 폰트 (Google Fonts) |
| `Jost` / `Noto Sans KR` | 본문 폰트 (Google Fonts) |
| CSS Variables | 테마 색상 관리 |
| Intersection Observer API | 스크롤 애니메이션 |
| YouTube IFrame API | MV 팝업 플레이어 |
| localStorage | 방명록 저장 |

외부 라이브러리 **없음** — 순수 바닐라 JS로 구현

---

## 📂 파일 구조

```
📁 newjeans-fan-archive/
└── index.html       ← 단일 파일 (HTML + CSS + JS 통합)
```

현재 단일 HTML 파일로 구성되어 있어 별도 빌드 과정 없이 바로 실행 가능합니다.

---

## 🚀 실행 방법

```bash
# 그냥 index.html을 브라우저에서 열면 됩니다.
open index.html
```

또는 로컬 서버를 사용하는 경우:

```bash
# Python 3
python -m http.server 8000

# VS Code Live Server 익스텐션 사용 권장
```

---

## 🎨 커스터마이징 가이드

추가하고 싶은 기능이 있다면 아래를 참고해주세요.

### 갤러리 이미지 교체
```html
<!-- index.html 내 gallery-item의 src를 변경 -->
<img src="여기에_이미지_URL" alt="설명">
```

### 멤버 정보 수정
`<!-- 01 MINJI -->` 주석을 찾아 `.m-name`, `.stat-val`, `.m-desc` 내용 수정

### 음악 플레이어 곡 목록 변경
```javascript
const SONGS = [
  { t: '곡 제목', d: 재생시간(초) },
  // 추가 가능
];
```

### 공연 정보 추가
`.concert-row` 블록을 복사해 날짜/장소 정보 입력

### 색상 테마 변경
```css
:root {
  --gold: #c8a96e;   /* 포인트 골드 컬러 */
  --bg:   #0d0b09;   /* 배경색 */
  /* 원하는 색상으로 변경 */
}
```

---

## 📋 업데이트 로그

| 날짜 | 변경 내용 |
|------|-----------|
| 2024 | 초기 버전 공개 |
| 2024 | 방명록 쿨다운 기능 추가 |
| 2024 | 반응형 모바일 레이아웃 개선 |

---

## 🚫 사용 제한 (License & Usage)

```
이 프로젝트는 팬 창작물로, 아래 행위를 금지합니다:

❌ 상업적 이용 (광고, 수익화, 유료 판매 등)
❌ 무단 재배포 또는 다른 플랫폼 업로드
❌ 원작자 표시 없는 도용
❌ ADOR · HYBE · 뉴진스의 공식 콘텐츠를 허가 없이 재업로드
❌ 이 코드를 이용한 피싱, 사기, 악의적 목적의 사이트 제작

✅ 허용: 개인 학습 목적의 코드 참고
✅ 허용: 동일한 팬 목적의 비영리 프로젝트 (출처 명시 필수)
✅ 허용: 버그 제보 및 개선 제안
```

---

## 💌 마치며

> 뉴진스를 좋아하는 마음 하나로 만들었습니다.  
> 민지, 하니, 다니엘, 해린, 혜인 — 언제나 응원합니다 🐰💛  
>  
> *This archive was built purely out of love for NewJeans.*  
> *민지 · 하니 · 다니엘 · 해린 · 혜인 — 영원히 함께해요.*

---

<div align="center">

🐰 **NewJeans Fan Archive** 🐰  
`비공식 팬 제작 · Unofficial Fan Project`  
All rights to NewJeans content belong to **ADOR · HYBE**

</div>
