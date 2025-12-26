# Flip Date

## Overview
- SVG flip-style date display with year, month, day, and day-of-week.
- Month and day use flip cards; year and DOW are static text.

## Runtime Dependencies
- SVG.js via CDN:
  `https://cdn.jsdelivr.net/npm/@svgdotjs/svg.js@3.2.4/dist/svg.min.js`

## Layout
- ViewBox is `0 0 560 300`.
- Card size: `150 x 120` with a `24` gap.
- Year centered above the cards; DOW label to the right.
- Optical vertical alignment uses `OPTICAL_NUDGE`.

## Flip Unit
- Top/bottom card split with clip groups and a flap for animation.
- Text baseline is computed from bbox center for visual centering.

## Behavior
- Tick runs once per second, aligned to the exact second.
- Date changes trigger flips:
  - Day card flips immediately.
  - Month card flips after `220ms` on month rollover.
  - Year text updates directly.
- Day-of-week color:
  - Saturday: blue
  - Sunday: red
  - Weekdays: muted gray

## Key Parameters
- `OPTICAL_NUDGE = 5`
- Flip duration: `650ms`

