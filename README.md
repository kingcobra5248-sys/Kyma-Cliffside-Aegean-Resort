# Kyma — Cliffside, Aegean

A single-page marketing site for **Kyma**, a fictional twelve-room cliffside resort on the Aegean coast of Greece. Built as one self-contained HTML file with embedded CSS and JavaScript — no build step, no dependencies to install.

## Preview

Open `kyma-resort.html` directly in any modern browser. A static PDF export (`kyma-resort.pdf`) and a 1200×630 social-preview thumbnail (`kyma-thumbnail.png`) are included alongside it.

## Sections

| Section | Content |
|---|---|
| **Hero** | Animated canvas sea/sky/cliff scene, headline, and quick-book actions |
| **Ticker** | Scrolling strip of brand taglines |
| **Concierge** | "Kalliope" AI concierge demo — clickable prompts trigger a typed chat reply |
| **Stay** | Bento-style grid of five room categories with pricing |
| **Experiences** | Horizontally scrollable cards (sailing, diving, yoga, wine tasting, dinner) |
| **Dine** | Two on-site restaurants |
| **Stats** | Animated count-up band (ratings, room count, etc.) |
| **Book** | Reservation form (front-end only, no submission handler) |
| **Footer** | Site links and contact details |

## Tech

- **Fonts:** Fraunces (display serif), Manrope (body), JetBrains Mono (labels) — loaded from Google Fonts
- **No frameworks** — vanilla HTML/CSS/JS in a single file
- **Canvas animation** for the hero sea/sky backdrop, drawn and animated with `requestAnimationFrame`
- **IntersectionObserver** for scroll-triggered reveal animations and the stat count-up
- **CSS custom properties** for the full color/typography system, defined in `:root`
- Responsive breakpoints at 900px, 800px, 760px, and 600px

## Interactive behaviors

- **Tide progress bar** (right edge, desktop only) — fills as the user scrolls down the page
- **Nav bar** — becomes opaque/blurred once scrolled past the hero
- **Concierge chat** — clicking a suggested prompt types out a canned AI response character-by-character; auto-triggers once the section scrolls into view
- **Room bento cards** — reveal a description on hover
- **Stat counters** — animate from 0 to their target value when scrolled into view

## Notes

- The booking form has no backend — submission is disabled (`onsubmit="return false;"`)
- All footer/journal links are placeholders (`href="#"`)
- Reduced-motion is respected via `prefers-reduced-motion`, which disables all animations and transitions
