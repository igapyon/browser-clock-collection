# Analog Clock + Flip Date

## Overview
- Analog clock rendered with SVG.
- Flip-style date cards (YYYY + MM + DD) plus Japanese day-of-week.
- Date block is positioned to avoid overlap with hands and kept inside the dial.

## Runtime Dependencies
- SVG.js via CDN:
  `https://cdn.jsdelivr.net/npm/@svgdotjs/svg.js@3.2.4/dist/svg.min.js`

## Layout
- ViewBox is `0 0 400 400` with center at `(200, 200)`.
- Dial radius: `172`.
- Date block is scaled by `0.62` and centered via `dateRoot.center(x, y)`.
- Clamp logic keeps the date block inside the viewBox (margin `10`).

## Date Block
- Year text above two flip cards (MM and DD).
- Day-of-week label to the right of the cards.
- Colors:
  - Saturday: blue (`theme.sat`)
  - Sunday: red (`theme.sun`)
  - Weekdays: muted (`theme.dowText`)

## Behavior
- Ticks are aligned to the next exact second using:
  `setTimeout(tickAlignedOncePerSecond, 1000 - d.getMilliseconds())`.
- Hands are rotated based on current time each tick.
- Date is updated only when the day changes (tracked by `lastDateKey`).
- Date block is placed on the side opposite the midpoint between hour and minute hands, with a small angle offset for balance.

## Key Parameters
- `DATE_SCALE = 0.62`
- Card size: `88 x 66`
- Card gap: `18`
- Year font size: `30`
- Flip card font size: `42`

