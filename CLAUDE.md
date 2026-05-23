# garben.tech — Personal Portfolio

Tyler Garben's personal site at [garben.tech](https://garben.tech). A minimal, single-page link hub inspired by the clean aesthetic of personal portfolio pages.

## Structure

```
index.html      — The entire site (self-contained, no build step)
img/
  favicon.ico   — Browser tab icon
  sipfolioLogo.png — Sipfolio app logo (available for use in app cards)
  me.png        — Profile photo
```

## Tech stack

- Pure HTML/CSS — no frameworks, no build tools
- Fonts: **Instrument Serif** (headings/accents) + **DM Sans** (body) via Google Fonts
- All styles are inline in `index.html` — intentionally no separate CSS file

## Design tokens

| Token | Value | Usage |
|---|---|---|
| `--bg` | `#0e0d0b` | Page background |
| `--surface` | `#161512` | Card backgrounds |
| `--surface-raised` | `#1c1b18` | Card hover state |
| `--accent` | `#c8a96e` | Gold highlights, Sipfolio icon |
| `--text-primary` | `#f0ece4` | Main text |
| `--text-secondary` | `#8c8880` | Subtitles, descriptions |
| `--text-muted` | `#565450` | Section labels, footer |

## Sections

1. **Intro** — Avatar (`T` monogram), name, tagline
2. **Apps** — `.app-card` links with icon, name, description, badge, arrow
3. **Find me** — `.social-link` pills (GitHub, Instagram, X, LinkedIn, Email)
4. **Footer** — simple muted one-liner

## Adding an app card

Copy this pattern inside `.apps`:

```html
<a class="app-card" href="URL" target="_blank" rel="noopener">
  <div class="app-icon CLASSNAME">EMOJI</div>
  <div class="app-info">
    <p class="app-name">App Name</p>
    <p class="app-desc">Short description here</p>
  </div>
  <span class="app-badge badge-beta">Beta</span>  <!-- or badge-wip -->
  <span class="app-arrow">→</span>
</a>
```

Badge options: `badge-beta` (gold), `badge-wip` (muted gray)

## App icon colors

- `sipfolio` — warm dark brown gradient, gold border
- `cradlelight` — cool dark blue gradient, blue border
- Add new classes following the same `linear-gradient(145deg, ...)` pattern

## Deployment

Static HTML — deploy by pushing to the hosting provider (GitHub Pages, Vercel, Netlify, etc.). No build step required.
