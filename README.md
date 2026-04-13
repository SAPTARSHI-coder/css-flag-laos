# CSS Flag — Flag of Laos

A pure CSS recreation of the national flag of Laos, constructed from three nested `<div>` elements and styled entirely through CSS — no images, no SVG, no added classes or IDs.

## Overview

The flag renders at 900×600px, centered on screen, and consists of three horizontal bands (red, blue, red) with a white circle centered on the blue band. The constraint of the exercise is to produce the correct result using only CSS combinators and selectors on the existing HTML structure.

## Flag Composition

| Layer | CSS Selector | Appearance |
|---|---|---|
| Outer div | `.flag` | Red background (`#ce1126`), 900×600px |
| Middle div | `.flag > div` | Blue band (`#002868`), absolutely positioned |
| Inner div | `.flag > div div` | White circle via `border-radius: 50%` |

## Tech Stack

| Technology | Role |
|---|---|
| HTML5 | Three nested `<div>` elements only |
| CSS3 | Colors, positioning, border-radius |

## Project Structure

```
css-flag-laos/
├── index.html      — Flag page with embedded solution CSS
├── solution.html   — Reference implementation
└── goal.png        — Target visual to replicate
```

## Getting Started

Open `index.html` in any browser. No internet connection or build step required.

## Key Concepts

- `position: relative` and `position: absolute` for layered layout
- `border-radius: 50%` to render a circle from a square element
- **Child combinator** selector (`.flag > div`, `.flag > div div`)
- CSS specificity and selector targeting without classes or IDs

