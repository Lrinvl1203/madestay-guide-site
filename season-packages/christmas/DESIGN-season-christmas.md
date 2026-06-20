---
version: alpha
name: Warm Christmas Concierge
description: 따뜻한 호텔 라운지 감성의 숙소 웹가이드 크리스마스 시즌 패키지.
colors:
  primary: "#241B16"
  secondary: "#7E6A55"
  tertiary: "#9F1D35"
  neutral: "#FBF6EE"
  surface: "#FFF9EF"
  accentGreen: "#0F5132"
  accentGold: "#C89B3C"
  line: "#E8D9C5"
typography:
  h1:
    fontFamily: Plus Jakarta Sans
    fontSize: 3rem
    fontWeight: 800
    lineHeight: 1.04
    letterSpacing: "-0.045em"
  h2:
    fontFamily: Plus Jakarta Sans
    fontSize: 1.5rem
    fontWeight: 750
    lineHeight: 1.25
    letterSpacing: "-0.035em"
  body-md:
    fontFamily: Pretendard
    fontSize: 1rem
    fontWeight: 500
    lineHeight: 1.65
rounded:
  sm: 12px
  md: 20px
  lg: 28px
  pill: 999px
spacing:
  xs: 6px
  sm: 10px
  md: 16px
  lg: 24px
  xl: 32px
components:
  hero-card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    rounded: "{rounded.lg}"
    padding: 28px
  button-primary:
    backgroundColor: "{colors.tertiary}"
    textColor: "#FFFFFF"
    rounded: "{rounded.pill}"
    padding: 12px
  chip-seasonal:
    backgroundColor: "#F7E8D0"
    textColor: "{colors.primary}"
    rounded: "{rounded.pill}"
    padding: 10px
---

## Overview

Warm Christmas Concierge는 숙소 웹가이드의 필수 안내 기능을 유지하면서 연말의 따뜻함을 더하는 시즌 디자인이다. 분위기는 쇼핑몰식 빨강/초록이 아니라 호텔 라운지, 우드 가구, 촛불, 금빛 조명, 조용한 눈 내림에 가깝다.

## Colors

- **Primary `#241B16`**: 본문과 제목의 짙은 브라운 잉크.
- **Tertiary `#9F1D35`**: 버건디 CTA와 시즌 포인트.
- **Accent Green `#0F5132`**: 크리스마스 그린. 큰 면적보다 badge, border, icon에 사용.
- **Accent Gold `#C89B3C`**: 조명, sparkle, focus ring, hover glow.
- **Neutral `#FBF6EE` / Surface `#FFF9EF`**: 따뜻한 종이와 아이보리 배경.

## Typography

Plus Jakarta Sans 또는 Pretendard를 사용한다. 제목은 크고 둥글게, 본문은 한국어 가독성을 우선한다. 시즌 문구는 짧고 따뜻하게 쓴다.

## Layout

모바일 480px max shell을 유지한다. SeasonalHero는 홈 상단 1개, SeasonalBento는 quick menu 아래 4개 카드로 제한한다.

## Elevation & Depth

카드는 부드러운 브라운 shadow와 gold glow를 사용한다. Glow는 CTA, hero, seasonal card에만 허용한다.

## Shapes

모든 주요 카드는 24~32px radius. 버튼과 chip은 pill 형태로 크리스마스 선물 리본 느낌을 준다.

## Components

- `SeasonalHero`: Merry Stay, check-in summary, snow layer.
- `SeasonalBadge`: Holiday picks, Warm route, Photo spot.
- `SeasonalBento`: 포토 스팟, 카페, 실내 코스, 체크아웃 마무리.
- `SeasonalAIChips`: 시즌 질문 4개.
- `SnowLayer`: hero 내부에서만 작동. prefers-reduced-motion에서 disable.

## Do's and Don'ts

Do:
- 운영 정보는 기존 레이아웃과 대비를 유지한다.
- 눈과 sparkle은 아주 느리고 작은 입자로 제한한다.
- 숙소 사진에는 warm overlay만 추가한다.

Don't:
- 원색 빨강/초록을 넓은 배경에 쓰지 않는다.
- 체크인/와이파이 정보를 장식 밑에 숨기지 않는다.
- Santa, 과한 캐릭터, 쇼핑몰 배너 톤을 쓰지 않는다.
