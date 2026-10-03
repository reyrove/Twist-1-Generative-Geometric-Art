# Twist 1 — Generative Art

> A seed-based generative system for glowing-circle compositions.  
> A reproducible catalogue of computational vibration studies.

---

## What is this?

**Twist 1** is a generative design system built on accumulation. One hundred to five hundred glowing rings are placed along a mathematical twist — each at its own angle, each with its own radius, each tinted from the RGB spectrum. The rings overlap; the colours blur; the field becomes a soft **vibration** rather than a drawing.

Every artwork in this catalogue is defined by a single numeric seed. The same seed always produces the identical composition — making each piece **traceable, reproducible, and licensable** across textile, print, and apparel applications.

Named for the helical drift that emerges from positioning circles along a sine–cosine arc, **Twist 1** reframes accumulation as a textile.

---

## Live

🌐 **[View the catalogue →](https://reyrove.github.io/Twist-1/)**

---

## The System

The generator is a single-layer system — a field of glowing rings whose positions, sizes, colours, and strokes are all seeded:

| Layer | Description |
|-------|-------------|
| **Ground** | One of 12 pastel background tones, chosen per seed. |
| **Rings** | 100 to 500 glowing circles positioned along a twist, each tinted from a low-range RGB noise function. |

Both layers are driven by the same seed, ensuring deterministic output.

### Parameters

- **Circle count** — 100 to 500 (stepped in tens)
- **Twist range** — π to 5π, seeding the arc and the shadow blur
- **Circle position** — along a sine/cosine arc, one-third of the canvas from centre
- **Circle radius** — proportional to the twist angle
- **Stroke weight** — `w / (30B)` to `w / (20B)`, seeded
- **Background** — drawn from 12 curated pastel tones

---

## Structure

```
Twist-1/
├── index.html              ← Full catalogue (single-file)
├── images/
│   ├── fav.svg
│   ├── twist-tote.png
│   ├── twist-cushion.png
│   └── ...
├── Twist-1.jpg             ← Apparel mockup
└── README.md
```

The entire project is contained in a single `index.html` — no build step, no dependencies, no framework. Open it in any modern browser.

---

## Features

- **Seed-based generation** — every composition is deterministic and reproducible
- **Live catalogue** — cover, statement, plate, surfaces, process, archive, commission sections
- **Multiple surfaces** — print, scarf, textile, wallpaper — all rendered from the same seed
- **Archive of 8 seeds** — click any plate to load it into the main view
- **PNG export** — download any composition directly from the browser
- **Keyboard shortcuts** — `R` for new seed, `S` to save
- **Legal modal** — licensing, terms, and credits built in
- **Responsive** — works on desktop, tablet, and mobile
- **Mobile-first navbar** — horizontally scrollable with fade hint

---

## Usage

### Generate a new composition

Click **New Seed** or press `R`.

### Download the current composition

Click **Download** or press `S`.

### Load a seed from the archive

Click any plate in the **Archive** section.

---

## Color System

Every composition is drawn from two curated palettes:

- **Background** — one of 12 pastel tones:

  | Hex | Name |
  |-----|------|
  | `#FFC0CB` | Pink |
  | `#FFA07A` | Light Salmon |
  | `#FFFFE0` | Light Yellow |
  | `#E6E6FA` | Lavender |
  | `#ADFF2F` | Green Yellow |
  | `#66CDAA` | Medium Aquamarine |
  | `#E0FFFF` | Light Cyan |
  | `#FFE4C4` | Bisque |
  | `#F5F5DC` | Beige |
  | `#DCDCDC` | Gainsboro |
  | `#FFF0F5` | Lavender Blush |
  | `#FFF8DC` | Cornsilk |

- **Circles** — each drawn from a low-range RGB noise function with a cool-green bias (`r: 0–192`, `g: 0–252`, `b: 0–208`), which keeps the field in a soft, saturated range rather than pure white or black.

Because both the twist and the RGB noise are seeded, no two compositions share the same rhythm of glow and hue.

---

## Technical Notes

- Pure vanilla JavaScript — no libraries
- Canvas 2D rendering
- Custom xorshift random generator for deterministic seeds
- Device-pixel-ratio aware rendering
- Fully static rendering — one seed produces one composition, no animation loops
- Single `renderStatic()` function drives the cover, plate, framed print, all four surfaces, and all eight archive thumbnails
- Glow via `shadowColor` + `shadowBlur` per circle stroke
- `prefers-reduced-motion` respected

---

## About

**Twist 1** is a project by [Reyhaneh Daneshdoost](https://reyrove.github.io/) — an Iranian-born artist working at the intersection of classical textile logic and generative systems.

The work begins with a simple observation: the woven surface — repetitive, mathematically structured, infinitely variable — has always been a form of computation, long before computers.

**Twist 1** is an attempt to render that logic visible.

> *A circle drawn from a distance becomes a vibration — and every vibration leaves a trace.*

---

## Licensing

All compositions are seed-documented and available for licensing across textile, surface, and apparel applications.

For commercial use, custom editions, or exclusive rights:

📧 **reyhanehdaneshdoost@gmail.com**

See the **Licensing** section in the live catalogue for details.

---

## Links

- 🌐 [Website](https://reyrove.github.io/)
- 📷 [Instagram](https://www.instagram.com/rey._.rove/)
- 💼 [LinkedIn](https://www.linkedin.com/in/reyhaneh-daneshdoost-730481160/)
- 🐦 [X](https://x.com/reyrove)

---

## Credits

**Design & Generative System**  
Reyhaneh Daneshdoost

**Typefaces**  
Cormorant Garamond · DM Mono

**Edition**  
Twist 1 — Autumn 2026

---

<p align="center">
  <em>Generative Glowing Circles</em><br />
  <sub>© Reyrove Studio · All compositions reproducible by seed</sub>
</p>