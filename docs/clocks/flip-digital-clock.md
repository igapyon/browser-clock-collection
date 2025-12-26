# Flip Digital Clock (24h)

## Overview
- SVG flip-style digital clock with hours, minutes, and seconds.
- Each unit uses a top/bottom split card and a flipping flap.

## Runtime Dependencies
- SVG.js via CDN:
  `https://cdn.jsdelivr.net/npm/@svgdotjs/svg.js@3.2.4/dist/svg.min.js`

## Layout
- ViewBox is `0 0 720 240`.
- Card size: `170 x 140`.
- Layout centers three cards (HH, MM, SS) with colon separators.
- Optical vertical alignment is controlled by `OPTICAL_NUDGE`.

## Flip Unit
- Uses clipped groups for top, bottom, and flap sections.
- Measures text bbox to compute a baseline that centers digits visually.
- Animation uses `easeInOutCubic` and scales the flap around the hinge line.

## Behavior
- Time updates once per second, aligned to the exact second.
- Flip sequencing:
  - Seconds flip immediately.
  - Minutes flip after `180ms`.
  - Hours flip after `360ms`.
- If a unit does not change, it is set without flipping.

## Key Parameters
- `OPTICAL_NUDGE = 6`
- Flip duration: `650ms`
- Separator font size: `64`

