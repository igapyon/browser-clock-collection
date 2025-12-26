# Analog Clock

## Overview
- SVG analog clock face with ticks and numerals.
- Three hands (hour, minute, second) updated once per second.

## Runtime Dependencies
- SVG.js via CDN:
  `https://cdn.jsdelivr.net/npm/@svgdotjs/svg.js@3.2.4/dist/svg.min.js`

## Layout
- ViewBox is `0 0 400 400` with center at `(200, 200)`.
- Dial radius: `172`.
- Mount size: `min(92vw, 420px)` with square aspect ratio.

## Rendering Notes
- Tick marks: 60 dots, with larger dots every 5 minutes.
- Numerals are drawn with a serif font; 10, 11, 12 are rendered as two separate glyphs for spacing control.
- Frame uses layered circles for highlights and shadow depth.

## Behavior
- Tick is aligned to the next exact second using:
  `setTimeout(tickAlignedOncePerSecond, 1000 - d.getMilliseconds())`.
- Hand rotation:
  - Hour: `hr * 30` degrees
  - Minute: `min * 6` degrees
  - Second: `sec * 6` degrees

## Key Parameters
- Dial radius: `172`
- Numeral font size: `42`
- Tick dot sizes: `5` (major), `3` (minor)

