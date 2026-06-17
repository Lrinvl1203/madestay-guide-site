---
version: alpha
name: MADE STAY Concierge
# Warm residential concierge UI for a mobile-first accommodation guide.
description: Warm editorial hospitality design with button-first navigation, Korean readability, and calm premium surfaces.
colors:
  primary: "#171411"
  secondary: "#5E554B"
  accent: "#C46F4B"
  accentDark: "#8F432A"
  sage: "#7F8F77"
  background: "#FBF8F3"
  paper: "#FFFDF8"
  cream: "#FFF8ED"
  line: "#E7DDD0"
typography:
  display:
    fontFamily: DM Sans, Noto Sans KR, system-ui
    fontSize: 3.8rem
    fontWeight: 900
    lineHeight: 1.03
    letterSpacing: "-0.07em"
  title:
    fontFamily: DM Sans, Noto Sans KR, system-ui
    fontSize: 2rem
    fontWeight: 900
    lineHeight: 1.12
    letterSpacing: "-0.05em"
  body:
    fontFamily: DM Sans, Noto Sans KR, system-ui
    fontSize: 1rem
    fontWeight: 500
    lineHeight: 1.72
    letterSpacing: "-0.02em"
rounded:
  sm: 14px
  md: 22px
  lg: 32px
  xl: 42px
spacing:
  xs: 8px
  sm: 12px
  md: 18px
  lg: 28px
  xl: 44px
components:
  menu-button:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.primary}"
    rounded: "{rounded.lg}"
    padding: 22px
  cta-primary:
    backgroundColor: "{colors.primary}"
    textColor: "#FFFFFF"
    rounded: 999px
    padding: 14px
---

## Overview

MADE STAY Concierge is a mobile-first guest guide, not a long landing page. The home screen should feel like a premium hotel remote control: a calm hero, the essential stay facts, and large thumb-friendly buttons. Guests should tap one button and enter exactly the topic they need.

## Colors

- **Primary / Night (#171411):** headline, primary CTA, and high contrast surfaces.
- **Accent / Terracotta (#C46F4B):** warmth, labels, active states, and visual anchors.
- **Background / Warm Ivory (#FBF8F3):** hospitality warmth instead of cold white.
- **Paper (#FFFDF8):** card surfaces.
- **Sage (#7F8F77):** quiet secondary emphasis.

## Typography

Use DM Sans with Noto Sans KR fallback. Korean copy must avoid cramped line-height; body text should stay around 1.65–1.75. Use strong weights for headings and button labels, but keep paragraphs medium-weight for readability.

## Layout

- Home = button hub only: no long text sections on first view.
- Every detail topic is a separate `.page` view entered by a button.
- Mobile first: buttons at least 64px tall, clear icon, title, and short hint.
- Desktop should preserve the same IA, widening into two-column cards rather than turning into a cluttered brochure.

## Components

- Menu buttons use paper cards, subtle shadow, large icon chip, and arrow affordance.
- Detail pages start with a compact hero and a sticky back/home action.
- Manual images must live inside the correct topic, not in a generic gallery.

## Do's and Don'ts

- Do make the main page a clean decision screen.
- Do keep original detailed guide content accessible.
- Do preserve map, phone, and source links.
- Don't place unrelated images under manual topics.
- Don't use tiny Linktree-like buttons or inconsistent spacing.
