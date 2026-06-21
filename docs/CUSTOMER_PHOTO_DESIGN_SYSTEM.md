# Customer Photo → Design System Workflow

고객이 모바일 가이드 제작을 위해 숙소 사진을 제공했을 때, 메인 사진의 분위기·톤·소재·조명감을 읽어 `design.md`를 만들고, 기존 `guide-woody-v2.html` 레이아웃에는 **구조 변경 없이 컬러/디자인 토큰만 적용**하기 위한 작업 규칙이다.

## Current Target

- Target page: `guide-woody-v2.html`
- Preserve: 현재 v2 홈 스켈레톤과 모든 화면 구조
  - Home order: Hero → time-aware smart card → quick menu → basic info
  - Screens: `home`, `wifi`, `appliances`, `laundry`, `trash`
  - Bottom tabs: 홈, 와이파이, 사용법, 세탁, 쓰레기
- Change only: visual design layer
  - colors
  - typography if needed
  - radius
  - shadow
  - card/button/nav visual treatments
  - hero image/tint if customer hero photo is approved

Do not reintroduce removed home sections:

- 빠른 안내 도우미 card on home
- 무엇을 확인할까요 menu-list section on home

## Input Photos

When photos are provided, classify them first:

```text
mainHeroPhoto        = best overall room/exterior/brand mood photo
secondaryMoodPhotos  = supporting ambience photos
operationalPhotos    = controls, QR, parking, trash, appliance photos
unsuitablePhotos     = blurry, private, duplicated, low-quality, privacy-sensitive
```

Only the `mainHeroPhoto` and `secondaryMoodPhotos` should drive the design concept. Operational photos should keep their semantic guide roles and should not define the whole visual concept unless they are also strong brand photos.

## Photo Analysis Checklist

For the selected main photo, extract:

1. Mood keywords
   - e.g. warm wood, urban calm, minimal hotel, bright airy, vintage, natural, resort, monochrome
2. Lighting
   - warm sunlight, cool daylight, evening mood, low-key, high-key, soft indirect light
3. Dominant palette
   - background neutral
   - surface/card color
   - text color
   - muted text color
   - primary accent
   - soft accent
   - border/line color
4. Material cues
   - wood, fabric, stone, concrete, metal, plants, glass, paper, leather
5. Shape language
   - rounded/tactile, minimal/sharp, soft organic, editorial, hotel-luxury
6. Typography direction
   - usually keep Pretendard for Korean readability unless a clear brand reason exists
7. Component implications
   - hero tint
   - smart card gradient
   - card surface
   - quick menu buttons
   - bottom nav
   - icon circle style
   - warnings/callouts

## `design.md` Template

Create a property-specific design file, e.g.:

```text
designs/<customer-or-property>.design.md
```

Recommended content:

```md
# <Property Name> Design System

## Source Photo

- Main photo: <filename or asset path>
- Supporting photos: <list>
- Concept name: <short name, e.g. Warm Walnut Stay>

## Visual Reading

- Mood: <3-6 keywords>
- Lighting: <description>
- Materials: <wood/fabric/stone/etc>
- Guest impression: <one-sentence guest-facing mood>

## Design Tokens

```css
:root {
  --bg: #...;
  --card: #...;
  --ink: #...;
  --muted: #...;
  --secondary: #...;
  --line: #...;
  --accent: #...;
  --accent-soft: #...;
  --danger: #...;
  --danger-soft: #...;
  --shadow: ...;
  --r: ...px;
  --r-btn: ...px;
  --hero: url('assets/...');
}
```

## Component Rules

- Body background: <rule>
- Hero treatment: <gradient/tint/object-position>
- Smart card: <gradient and contrast rule>
- Cards: <surface/border/shadow/radius>
- Quick menu: <button surface/icon color>
- Bottom nav: <fixed; preserve 5 columns; active state>
- Chat/floating buttons: <accent treatment>

## Preserve

- Do not change page order or routing.
- Do not change content values such as Wi-Fi, trash instructions, appliance instructions.
- Do not replace Material Symbols with image icons unless explicitly requested.
- Do not move operational images into decorative slots.
```

## CSS Application Pattern

In `guide-woody-v2.html`, apply a generated design by changing tokens and a final override block only. Preserve the DOM.

Minimum token mapping:

```css
:root{
  --bg: ...;
  --card: ...;
  --ink: ...;
  --muted: ...;
  --secondary: ...;
  --line: ...;
  --bronze: ...;       /* current V2 accent alias */
  --bronze-soft: ...;  /* current V2 soft accent alias */
  --soft: ...;
  --shadow: ...;
  --r: ...;
  --r-btn: ...;
  --hero: url('...');
}
```

If the new design uses `--accent`, map it to existing aliases:

```css
--bronze: var(--accent);
--bronze-soft: var(--accent-soft);
--soft: var(--accent-soft);
```

## Verification Checklist

After applying a design:

```js
JSON.stringify({
  title: document.title,
  screens: [...document.querySelectorAll('[data-screen]')].map(e => e.dataset.screen),
  homeOrder: [...document.querySelector('.screen[data-screen="home"]').children].map(e => e.className || e.tagName),
  quickLabels: [...document.querySelectorAll('.screen[data-screen="home"] .quick button')].map(b => b.innerText.replace(/\s+/g,' ').trim()),
  forbidden: {
    quickAssistant: document.body.innerText.includes('빠른 안내 도우미'),
    whatToCheck: document.body.innerText.includes('무엇을 확인할까요?'),
    menuList: !!document.querySelector('.screen[data-screen="home"] .menu-list')
  },
  bottomPosition: getComputedStyle(document.querySelector('.bottom')).position,
  bottomColumns: getComputedStyle(document.querySelector('.bottom')).gridTemplateColumns,
  bodyBg: getComputedStyle(document.body).backgroundColor,
  badImages: [...document.images].filter(i => !i.complete || !i.naturalWidth).map(i => i.src)
})
```

Expected:

- `screens`: `home,wifi,appliances,laundry,trash`
- `homeOrder`: hero → smart-card → quick → basic-info card
- `quickLabels`: 와이파이, TV 및 미디어, 냉·난방, 세탁
- `forbidden.quickAssistant`: false
- `forbidden.whatToCheck`: false
- `forbidden.menuList`: false
- `bottomPosition`: fixed
- `badImages`: []

## Production Workflow

1. Save customer photos under a clear folder, e.g. `assets/customer/<property>/source/`.
2. Choose and optimize the hero photo into `assets/customer/<property>/hero.webp`.
3. Create `designs/<property>.design.md`.
4. Apply design tokens to a new variant first if comparison is needed, or to `guide-woody-v2.html` if the user explicitly wants v2 updated.
5. Verify locally with browser.
6. Commit and deploy.
7. Verify production URL with cache-busting query.

## Pitfalls

- Do not let a beautiful room photo override operational image semantics.
- Do not change v2 structure while applying a design.
- Do not add back old home sections that were intentionally removed.
- Do not use v3 Stitch image icons in v2 unless explicitly requested.
- Keep Korean guest-facing labels polished and avoid implementation language such as `design.md`, tokens, source, or build on the visible page.
