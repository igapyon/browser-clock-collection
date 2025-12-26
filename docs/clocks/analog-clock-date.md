# Analog Clock + Flip Date (Mini)

## Overview
- Analog clock rendered with SVG.
- Flip-style date mini (YYYY + MM + DD) plus Japanese day-of-week.
- Date block is positioned on the outer angle between hour and minute hands.

## Runtime Dependencies
- SVG.js via CDN:
  `https://cdn.jsdelivr.net/npm/@svgdotjs/svg.js@3.2.4/dist/svg.min.js`

## Layout
- ViewBox is `0 0 400 400` with center at `(200, 200)`.
- Dial radius: `172`.
- Date block is built on a `560 x 300` layout and scaled by `DATE_SCALE`.
- Positioning uses `dateRoot.center(x, y)` with clamp to keep it inside the viewBox.

## Date Block
- Year text above two flip cards (MM and DD).
- Day-of-week label to the right/below of the cards.
- Colors:
  - Saturday: blue (`theme.sat`)
  - Sunday: red (`theme.sun`)
  - Weekdays: muted (`theme.dowText`)

## Behavior
- Ticks are aligned to the next exact second using:
  `setTimeout(tickAlignedOncePerSecond, 1000 - d.getMilliseconds())`.
- Hands are rotated based on current time each tick.
- Date is updated only when the day changes (tracked by `lastDateKey`).
- Day/month updates animate with flip; year and DOW update directly.
- Date block is placed on the side opposite the midpoint between hour and minute hands, with a small angle offset for balance.

## Key Parameters
- `DATE_SCALE = 0.3`
- Date layout size: `560 x 300`
- Card size: `90 x 72`
- Card gap: `14`
- Year font size: `44`
- DOW font size: `36`
- Outer radius: `dialR * 0.32`
