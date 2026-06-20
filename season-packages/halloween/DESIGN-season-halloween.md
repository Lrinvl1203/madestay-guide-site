---
version: alpha
name: Midnight Halloween Stay
description: 프리미엄 다크 톤의 숙소 웹가이드 할로윈 시즌 패키지.
colors:
  primary: "#FFF7ED"
  secondary: "#B7A8C9"
  tertiary: "#FF7A1A"
  neutral: "#100B18"
  surface: "#1F162D"
  accentPurple: "#8B5CF6"
  accentMoon: "#F4D98B"
  line: "#3C2B52"
typography:
  h1:
    fontFamily: Plus Jakarta Sans
    fontSize: 2.75rem
    fontWeight: 800
    lineHeight: 1.04
    letterSpacing: "-0.045em"
  h2:
    fontFamily: Plus Jakarta Sans
    fontSize: 1.45rem
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
    textColor: "#160D05"
    rounded: "{rounded.pill}"
    padding: 12px
  chip-seasonal:
    backgroundColor: "#2C2040"
    textColor: "{colors.primary}"
    rounded: "{rounded.pill}"
    padding: 10px
---

## Overview

Midnight Halloween Stay는 무섭거나 유치한 할로윈이 아니라 프리미엄한 밤 산책, 달빛, 안개, 보라/오렌지 글로우를 활용한 숙소 웹가이드 시즌 디자인이다.

## Colors

- **Neutral `#100B18`**: 전체 배경의 딥 미드나잇.
- **Surface `#1F162D`**: glass card와 guide panel.
- **Tertiary `#FF7A1A`**: 호박빛 CTA, active state, focus.
- **Accent Purple `#8B5CF6`**: 테두리 glow와 dark UI depth.
- **Accent Moon `#F4D98B`**: moon highlight와 작은 badge.

## Typography

크고 단단한 제목과 높은 대비의 본문을 사용한다. 본문 크기는 줄이지 않는다. 다크 모드에서는 `primary`와 `secondary` 대비를 유지한다.

## Layout

기존 모바일 shell, 하단 nav, accordion 구조를 유지한다. Halloween 장식은 hero와 seasonal picks에만 적용한다.

## Elevation & Depth

카드는 glass 느낌의 어두운 surface, 보라/오렌지 glow, 얇은 line을 사용한다. 과한 neon은 금지한다.

## Shapes

모바일 카드 24~32px radius. 다크 테마에서도 버튼/정보 카드의 tap target은 44px 이상.

## Components

- `SeasonalHero`: Halloween Night Guide, moon glow, fog layer.
- `SeasonalBadge`: Night picks, Photo spot, Quiet hours.
- `SeasonalBento`: 포토존, 밤 산책, 안전 체크, 숙소 매너.
- `SeasonalAIChips`: 시즌 질문 4개.
- `FogLayer`: hero 내부에서만 작동. prefers-reduced-motion에서 disable.

## Do's and Don'ts

Do:
- 다크 모드 텍스트 대비를 우선한다.
- 할로윈 요소는 moon, fog, glow, pumpkin icon 정도로 절제한다.
- 이용수칙은 진지하고 명확하게 유지한다.

Don't:
- 피, 해골, 과한 귀신 이미지를 쓰지 않는다.
- 모든 메뉴명을 장난스럽게 바꾸지 않는다.
- 어두운 배경에서 회색 텍스트를 너무 낮은 대비로 두지 않는다.
