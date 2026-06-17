---
name: Serene Hospitality
colors:
  surface: '#fbf9f4'
  surface-dim: '#dbdad5'
  surface-bright: '#fbf9f4'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f5f3ee'
  surface-container: '#f0eee9'
  surface-container-high: '#eae8e3'
  surface-container-highest: '#e4e2dd'
  on-surface: '#1b1c19'
  on-surface-variant: '#444748'
  inverse-surface: '#30312e'
  inverse-on-surface: '#f2f1ec'
  outline: '#747878'
  outline-variant: '#c4c7c7'
  surface-tint: '#5f5e5e'
  primary: '#000000'
  on-primary: '#ffffff'
  primary-container: '#1c1b1b'
  on-primary-container: '#858383'
  inverse-primary: '#c8c6c5'
  secondary: '#715a3e'
  on-secondary: '#ffffff'
  secondary-container: '#fdddb9'
  on-secondary-container: '#786044'
  tertiary: '#000000'
  on-tertiary: '#ffffff'
  tertiary-container: '#1b1c1c'
  on-tertiary-container: '#848484'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e5e2e1'
  primary-fixed-dim: '#c8c6c5'
  on-primary-fixed: '#1c1b1b'
  on-primary-fixed-variant: '#474746'
  secondary-fixed: '#fdddb9'
  secondary-fixed-dim: '#e0c29f'
  on-secondary-fixed: '#281803'
  on-secondary-fixed-variant: '#584329'
  tertiary-fixed: '#e3e2e2'
  tertiary-fixed-dim: '#c7c6c6'
  on-tertiary-fixed: '#1b1c1c'
  on-tertiary-fixed-variant: '#464747'
  background: '#fbf9f4'
  on-background: '#1b1c19'
  surface-variant: '#e4e2dd'
typography:
  display:
    fontFamily: Manrope
    fontSize: 48px
    fontWeight: '600'
    lineHeight: 56px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Manrope
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-lg-mobile:
    fontFamily: Manrope
    fontSize: 28px
    fontWeight: '600'
    lineHeight: 34px
  headline-md:
    fontFamily: Manrope
    fontSize: 24px
    fontWeight: '500'
    lineHeight: 32px
  body-lg:
    fontFamily: Manrope
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Manrope
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-md:
    fontFamily: Manrope
    fontSize: 14px
    fontWeight: '600'
    lineHeight: 20px
    letterSpacing: 0.05em
  caption:
    fontFamily: Manrope
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 8px
  xs: 4px
  sm: 12px
  md: 24px
  lg: 40px
  xl: 64px
  container-max: 1200px
  gutter: 20px
---

## Brand & Style
The design system is centered on the concept of "Mindful Hospitality," specifically tailored for the premium digital concierge experience of MADE STAY 301. The brand personality is calm, warm, and highly organized, reflecting the meticulous care of a boutique Seoul stay. 

The aesthetic blends **Modern Minimalism** with **Tactile Softness**. It avoids the coldness of typical SaaS products by utilizing a warm, organic color palette and generous whitespace that evokes a sense of physical space and breathability. The emotional response should be one of immediate relief and trust—moving the guest from the chaos of travel into a curated, serene sanctuary.

## Colors
The palette is grounded in warm, earth-toned neutrals to create an inviting atmosphere. 
- **Background (#F9F7F2):** A warm ivory that acts as the canvas, reducing eye strain and feeling more "editorial" than pure white.
- **Surface (#FFFFFF):** Pure white is reserved for cards and interactive containers to provide a crisp lift from the ivory base.
- **Primary Text (#1A1A1A):** A deep charcoal, almost black, ensuring high legibility and an authoritative, premium feel.
- **Accents (#8C7355):** A warm bronze used sparingly for call-to-actions, active states, and premium highlights.
- **Secondary Text (#767676):** A muted taupe gray for metadata, labels, and non-essential information to maintain visual hierarchy.

## Typography
This design system utilizes **Manrope** for its balanced, modern, and highly legible characteristics. The hierarchy is intentionally dramatic to guide guests through concierge services effortlessly.

- **Headlines:** Use tighter letter-spacing and medium-to-semibold weights to feel grounded.
- **Labels:** Small caps or uppercase with increased tracking (0.05em) are used for category headers and utility labels to provide a sophisticated, "hotel stationery" feel.
- **Body Text:** Standard weight with generous line-height (1.5x+) to ensure readability for international guests.

## Layout & Spacing
The layout follows a **Fluid Grid** model with generous outer margins (24px on mobile, up to 64px on desktop) to reinforce the premium, uncrowded feel.

- **Vertical Rhythm:** Use the `lg` (40px) unit between major sections to allow the eye to rest.
- **Mobile-First:** Elements should primarily use a single-column stack on mobile, moving to a staggered 2-column masonry or 3-column grid for tablet/desktop to mimic a lifestyle magazine.
- **Tap Targets:** All interactive elements must maintain a minimum height of 48px, though 56px is preferred for primary concierge actions.

## Elevation & Depth
Depth is created through **Tonal Layering** and **Ambient Shadows** rather than harsh borders.

1. **Base Layer:** The ivory background (#F9F7F2).
2. **Elevated Layer:** White cards (#FFFFFF) with a very soft, diffused shadow (0px 4px 20px rgba(26, 26, 26, 0.04)). This creates a "lifted paper" effect.
3. **Interactive Layer:** Active states may use a slightly deeper shadow or a subtle 1px stroke in the accent color (#8C7355) to indicate focus.

Avoid heavy blurs or glassmorphism; the goal is a physical, tactile feel that mimics high-quality paper and wooden finishes.

## Shapes
The shape language is characterized by large, organic curves that feel approachable and high-end. 

- **Primary Cards:** Use a 24px radius to soften the interface and frame content elegantly.
- **Buttons and Inputs:** Use a 12px radius, providing a slightly more structured look than the cards to denote utility.
- **Icons:** Should be thin-line (1.5px stroke) with slightly rounded terminals to match the typography.

## Components
- **Buttons:** Primary buttons are solid Charcoal (#1A1A1A) with White text. Secondary buttons are Ivory (#F9F7F2) with a thin Bronze (#8C7355) border. No "ghost" buttons; every action should feel intentional.
- **Cards:** White backgrounds with 24px padding. They should never have dark borders—only the soft ambient shadow mentioned in the Elevation section.
- **Inputs:** Floating label style with a subtle bottom border or a very light taupe stroke. Focus state transitions the border to Bronze (#8C7355).
- **Concierge Chips:** Small, rounded-pill tags used for "Available Now," "Room Service," or "Local Guide." These use the Bronze accent color with 10% opacity for the background and solid Bronze for the text.
- **Lists:** Clean, borderless list items separated by 1px Taupe (#767676) lines at 10% opacity. Icons in lists should always be aligned to the left with generous padding.
- **Navigation:** A bottom-anchored bar for mobile with haptic-ready icons and a clean, centered "Action" button for immediate guest assistance.