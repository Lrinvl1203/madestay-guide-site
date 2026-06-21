# REX.design.md

## Overview
- Property: 렉스 (REX)
- Variant target: `guide-rex-v2.html`
- Base skeleton: Woody V2 standard layout
- Intent: keep the proven V2 information architecture and apply only the visual concept extracted from the main room photos

## Concept Summary
REX는 **조용하고 정돈된 도심형 스테이**다. 사진에서 읽히는 핵심은 과한 럭셔리나 장식성이 아니라, **웜 뉴트럴 벽면**, **토프 브라운 커튼**, **포레스트 그린 침구**, **라이트 오크 우드**, **브라스 계열 조명**이 만드는 차분한 안정감이다.

Recommended concept label:
- **Quiet Urban Stay**
- **Warm Taupe & Forest Green**
- **Soft Brass Glow**

## Mood Keywords
- 도심형 차분함
- 부티크 생활형 스테이
- 웜 뉴트럴
- 패브릭 + 우드 + 브라스
- 낮에는 맑고, 밤에는 따뜻한 조명감
- 정돈된 휴식감

## Visual Reading Notes
### Main identity colors
- Warm Linen wall tone
- Taupe brown curtains
- Deep forest green bedding
- Pale oak / light wood furniture
- Warm brass lamp accent

### Important interpretation rule
- TV 화면의 빨강/파랑은 **공간 자체의 브랜드 컬러가 아니다**.
- 따라서 UI 메인 포인트 컬러는 TV 콘텐츠 색에서 가져오지 않는다.
- 공간 고유의 디자인 토큰은 **벽/커튼/침구/우드/조명**에서 추출한다.

## Design Tokens
### Core palette
- `--bg: #F5F1EB` — Warm Linen
- `--card: #FCFAF6` — Soft Ivory
- `--ink: #2B2623` — Warm Charcoal
- `--muted: #766B62` — Taupe Gray
- `--secondary: #5D5955` — Dusty Brown Gray
- `--line: #D9CEC2` — Soft Divider Beige
- `--accent: #35584B` — Forest Green
- `--accent-warm: #A88157` — Brass Taupe
- `--accent-soft: #EEE5D9` — Cream Sand
- `--success: #35584B`
- `--warning: #B4854E`

### Surface system
- 카드 표면은 **순백이 아닌 크림 화이트**
- 배경은 **살짝 톤다운된 리넨 아이보리**
- 그림자는 **짙지 않고 넓게 퍼지는 소프트 섀도우**
- 포인트 카드는 딥 그린 + 브라스 웜 그라데이션 허용

### Typography direction
- Korean body: Pretendard
- Optional heading support: Plus Jakarta Sans or similarly clean geometric sans
- 전체 톤은 단정하고 과장 없는 premium-lite 방향
- 굵기는 과도하게 무겁지 않게, 제목만 또렷하게

### Radius / shape
- 카드와 버튼은 부드러운 라운드
- 지나치게 sharp하거나 techy한 모서리는 피함
- tactile하지만 귀엽게 가지 않음

## Component Guidance
### Hero
- 메인 사진을 크게 사용하되 너무 어둡게 덮지 않는다
- 공간의 햇살/조명 온도를 살리는 밝은 오버레이 사용
- 카피는 짧고 안정적인 톤 유지

### Smart card
- 포레스트 그린을 메인 기반으로 사용 가능
- 브라스/토프를 서브 하이라이트로 사용
- 텍스트 대비는 충분히 확보

### Quick menu / bottom nav
- Standard V2 계열은 **Material/line icon system 유지**
- 이미지 아이콘 / isometric 아이콘 사용 금지
- active state는 forest green 계열이 적합

### Cards / list / chips
- 카드 내부는 넉넉한 여백
- 칩은 웜 아이보리 또는 투명 화이트 계열
- 보조 설명은 taupe gray로 낮은 대비 유지

## Do / Don’t
### Do
- 웜 아이보리 배경 사용
- 깊은 녹색을 제한된 포인트 컬러로 사용
- 우드/패브릭/브라스의 차분한 질감 해석 유지
- 구조는 V2 skeleton 그대로 유지
- 숙소별 파일명/타이틀 분리 (`guide-rex-v2.html`처럼)

### Don’t
- TV 화면 색을 메인 브랜딩 색으로 채택하지 않기
- 네온/사이버/고채도 블루·레드 사용 금지
- 이미지 아이콘, isometric 오브젝트 사용 금지 (standard V2 계열)
- 검정 대비를 과도하게 올려 luxury-black 방향으로 보내지 않기
- 레이아웃 자체를 다시 설계하지 않기

## Implementation Rule for Future Customer Photos
1. 숙소 이름을 먼저 받아서 **별도 배포 파일명**을 만든다.
2. 메인 사진 1장을 기준으로 무드 분석을 한다.
3. 보조 사진으로 색/재질/조명/공간감을 교차 검증한다.
4. `design.md`를 먼저 만든다.
5. V2 skeleton은 유지하고 token/CSS만 바꾼다.
6. 운영 정보가 없으면 임의의 실제 값으로 채우지 않는다.

## Suggested File Naming
- HTML: `guide-rex-v2.html`
- Design doc: `REX.design.md`
- Assets: `assets/rex/`

## Current Asset Set
- `assets/rex/rex-room-01.jpeg`
- `assets/rex/rex-room-02.jpeg`
- `assets/rex/rex-room-03.jpeg`
- `assets/rex/rex-room-04.jpeg`
- `assets/rex/rex-room-05.jpeg`
