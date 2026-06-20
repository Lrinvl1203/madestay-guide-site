# 웹가이드 시즌 이벤트 패키지 리서치

작성 목적: 기존 숙소 웹가이드의 모바일 사용성은 유지하면서, 크리스마스/할로윈 등 시즌별 감성과 추천 콘텐츠를 교체 가능한 패키지로 적용하기 위한 기준 문서.

## 1. 조사 결론

시즌 패키지는 단순한 배경 애니메이션이 아니라 **숙소 운영 정보 + 시즌 감성 + 주변 추천 + AI 질문 chip**을 함께 바꾸는 구조가 적합하다.

- 운영 정보: 체크인, 와이파이, 주차, 쓰레기, 가전 사용법은 변하지 않는다.
- 시즌 정보: 홈 hero, 추천 카드, 배경 레이어, 아이콘, AI 질문 chip만 바뀐다.
- 구현 방식: 기존 V5/우디 V3 모바일 앱형 스켈레톤을 보존하고 `data-season` 또는 별도 시즌 variant HTML로 적용한다.

## 2. 레퍼런스별 활용

| 소스 | 조사 포인트 | 웹가이드 적용 |
|---|---|---|
| Mobbin | 실제 모바일 앱의 홈, 카드, 추천, 여정, 온보딩 패턴 | 게스트가 QR로 열었을 때 바로 이해되는 quick action, 정보 카드, 추천 리스트 |
| 21st.dev | 커뮤니티 제작 React/Tailwind 컴포넌트, hero, bento, sparkle, AI chat | SeasonalHero, SeasonalBento, Sparkle/Fog layer, AI suggestion chips |
| Magic UI | particles, marquee, aurora text 등 장식성 높은 모션 컴포넌트 | 제한된 영역의 snow/fog/sparkle, 시즌 배너 ribbon |
| Aceternity UI | animated landing/card/glow/motion patterns | 고급스러운 card glow, dark glass Halloween, premium Christmas light |
| shadcn/ui / shadcnblocks | 접근성 좋은 accordion, tab, drawer, card primitive | 기존 가이드 구조의 안정적인 interaction 유지 |
| Airbnb | 숙박/여행의 사진 중심 warm UX | 숙소 사진 hero, 주변 추천 카드, 따뜻한 카피 |
| Apple | 프리미엄 여백, 계절 campaign 감성 | 과하지 않은 크리스마스, 고급스러운 typography |
| Stripe | gradient, soft depth, premium web | Christmas gold glow, seasonal CTA depth |
| Linear | 다크 모드, precision glow | Halloween premium dark, 보라/오렌지 border glow |
| Notion | 안내문, FAQ, checklist readability | 이용수칙/체크아웃 정보의 가독성 보존 |

## 3. 컴포넌트 후보

### 21st.dev 계열에서 차용할 패턴

- Aurora Background: 크리스마스 겨울 밤하늘 또는 할로윈 달빛 배경. 전체 화면이 아니라 hero 내부에만 제한.
- Sparkles / Sparkles Text: 크리스마스 조명/눈송이. 타이틀 주변만 사용.
- Bento Grid: 시즌 추천 4개 카드. 모바일에서는 1열/2열로 축소.
- Display Cards: quick action과 seasonal pick cards.
- Expandable Tabs: 시즌 안내, 주변 추천, 유의사항을 접이식으로 구성.
- Animated Hero: 첫 화면 seasonal welcome.
- AI Chat Components: 시즌 질문 chip, quick prompt, assistant panel.
- Tubelight Navbar: 하단 탭의 시즌 accent. 과하면 접근성 저하라 subtle mode만 사용.
- Infinite Ribbon / Marquee: “Holiday picks”, “Night spots” 같은 짧은 ribbon. 운영 정보 영역에는 사용하지 않음.

### Magic UI / Aceternity 계열

- Particles: snow/fog 입자. `prefers-reduced-motion`에서 꺼야 함.
- Marquee: 시즌 태그 흐름. 광고처럼 보이지 않게 속도 느리게.
- Glow / Spotlight Card: CTA와 recommendation에만 적용.
- Glass Card: Halloween에서 유리 카드 느낌.

## 4. Christmas 최적화 방향

### 콘셉트

**Warm Christmas Concierge** — 따뜻한 호텔 라운지, 우드, 아이보리, 딥 그린, 버건디, 골드, 은은한 눈.

### 적용 콘텐츠

- Hero title: `Merry Stay`
- Subtitle: `따뜻한 연말을 위한 스테이 가이드`
- Seasonal cards:
  1. 연말 포토 스팟
  2. 따뜻한 카페 추천
  3. 겨울 실내 코스
  4. 체크아웃 전 따뜻한 마무리
- AI chips:
  - 근처 크리스마스 분위기 좋은 카페
  - 연말 저녁 먹기 좋은 곳
  - 추운 날 실내 데이트 코스
  - 숙소에서 따뜻하게 쉬는 법

### 디자인 규칙

- 눈 효과는 hero 안에서만 사용한다.
- 빨강/초록 원색보다 버건디/딥그린/골드 중심.
- 체크인/와이파이 정보는 장식보다 먼저 보여야 한다.
- 숙소 사진에 warm overlay를 얹어 계절감만 추가한다.

## 5. Halloween 최적화 방향

### 콘셉트

**Midnight Halloween Stay** — 다크 네이비/블랙, 퍼플, 오렌지, 달빛, 안개, 글로우. 무섭기보다 프리미엄한 야간 이벤트.

### 적용 콘텐츠

- Hero title: `Halloween Night Guide`
- Subtitle: `밤 산책과 포토 스팟을 위한 특별 가이드`
- Seasonal cards:
  1. 할로윈 포토존
  2. 밤 산책 코스
  3. 아이와 함께라면 안전 체크
  4. 조용한 밤을 위한 숙소 매너
- AI chips:
  - 근처 할로윈 분위기 나는 곳
  - 밤에 산책하기 좋은 코스
  - 아이와 갈 만한 실내 장소
  - 비 오는 날 할로윈 코스

### 디자인 규칙

- 피/해골/공포 이미지 금지. 숙소 브랜드 신뢰도가 떨어진다.
- 다크 테마는 대비를 반드시 확보한다.
- 이용수칙을 장난스럽게 바꾸지 않는다.
- fog/glow는 hero와 seasonal cards에만 제한한다.

## 6. 구현 구조

권장 구조:

```text
season-packages/
├─ base/
│  ├─ season-loader.js
│  └─ README.md
├─ christmas/
│  ├─ tokens.css
│  ├─ seasonal-content.json
│  └─ DESIGN-season-christmas.md
└─ halloween/
   ├─ tokens.css
   ├─ seasonal-content.json
   └─ DESIGN-season-halloween.md
```

적용 방식:

1. PoC: `guide-seasonal-event.html` 하나에서 Christmas/Halloween toggle로 비교.
2. 고객용: `?season=christmas`, `?season=halloween` URL 파라미터 또는 호스트 설정값으로 제어.
3. 장기: Valentine, Cherry Blossom, Summer, New Year도 같은 schema로 확장.

## 7. 검증 체크리스트

- [ ] 390/430/480px 모바일에서 hero와 하단 nav가 깨지지 않는다.
- [ ] 체크인/와이파이/쓰레기 등 핵심 정보가 시즌 장식보다 우선한다.
- [ ] 다크 테마 텍스트 대비가 충분하다.
- [ ] `prefers-reduced-motion`에서 snow/fog animation이 꺼진다.
- [ ] AI chip은 시즌 추천만 담당하고 비공개 운영 정보를 추측하지 않는다.
- [ ] 기존 웹가이드 파일은 덮어쓰지 않는다.
