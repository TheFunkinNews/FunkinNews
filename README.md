<div align="center">

<img src="https://img.shields.io/badge/Funkin'%20News-The%20Mod%20Gazette-bf00ff?style=for-the-badge&labelColor=0a0010&color=bf00ff" alt="Funkin' News"/>

<br/>
<br/>

**A community-driven news hub for the Friday Night Funkin' ecosystem.**
Covering mods, engines, updates, and developer releases — all in one place.

<br/>

[![GitHub Pages](https://img.shields.io/badge/Live%20Site-GitHub%20Pages-00cfff?style=flat-square&logo=github&logoColor=white&labelColor=0a0010)](https://thefunkinnews.github.io/FunkinNews/)
[![License](https://img.shields.io/github/license/TheFunkinNews/FunkinNews?style=flat-square&labelColor=0a0010&color=bf00ff)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/TheFunkinNews/FunkinNews?style=flat-square&labelColor=0a0010&color=ff00aa)](https://github.com/TheFunkinNews/FunkinNews/stargazers)
[![Last Commit](https://img.shields.io/github/last-commit/TheFunkinNews/FunkinNews?style=flat-square&labelColor=0a0010&color=00ff88)](https://github.com/TheFunkinNews/FunkinNews/commits/main)

</div>

---

## Overview

**Funkin' News** is a static, single-page web application built with vanilla HTML, CSS, and JavaScript. It serves as a themed news portal for the FNF modding community, featuring a dark neon aesthetic inspired by the original game's visual identity.

The site is fully self-contained in a single `index.html` file with no external dependencies beyond Google Fonts, making it trivially deployable on GitHub Pages or any static host.

---

## Features

| Feature | Description |
|---|---|
| Breaking News Ticker | Animated scrolling headline bar at the top of the page |
| Hero Section | Featured post with full-width art and three side story cards |
| News Feed | Responsive 2-column grid with color-coded category tags |
| Featured Mods | Ranked sidebar list with gold/silver/bronze placement |
| Live Search | Client-side search with instant dropdown results |
| Community Stats | Live-feel counter panel for mods, engines, and devs |
| Tag Cloud | Clickable popular topic tags |
| Scanline Overlay | CSS-only CRT scanline effect for retro aesthetic |
| Glitch Animation | Logo text glitch effect on a 5-second loop |
| Fully Responsive | Collapses gracefully to single-column on mobile |

---

## Tech Stack

- **HTML5 / CSS3 / Vanilla JS** — zero build tools, zero frameworks
- **Google Fonts** — `Press Start 2P`, `VT323`, `Rajdhani`
- **GitHub Pages** — static hosting via the `main` branch root

---

## Project Structure

```
FunkinNews/
├── index.html        # Entire application — markup, styles, and logic
├── README.md         # This file
└── LICENSE           # Apache 2.0
```

---

## Getting Started

### View Locally

No build step required. Just open the file directly in any browser:

```bash
git clone https://github.com/TheFunkinNews/FunkinNews.git
cd FunkinNews
open index.html
```

Or with a local server to avoid font loading issues:

```bash
npx serve .
```

### Deploy to GitHub Pages

1. Go to the repository **Settings**
2. Navigate to **Pages** in the sidebar
3. Under **Source**, select **Deploy from a branch**
4. Set branch to `main`, folder to `/ (root)`
5. Save — the site will be live at `https://thefunkinnews.github.io/FunkinNews/` within a few minutes

---

## Customization

All content is hardcoded inside `index.html`. To update the site:

### Adding a News Card

Find the `<div class="news-list" id="newsGrid">` block and insert a new card:

```html
<div class="news-card">
  <div class="news-card-art purple">🎵</div>
  <div class="news-card-body">
    <span class="news-card-tag tag-mod">MOD</span>
    <h3>YOUR HEADLINE HERE</h3>
    <p>Short description of the news item.</p>
    <div class="news-meta">
      <span class="date">DD MMM</span>
      <span>@author</span>
    </div>
  </div>
</div>
```

Available art color classes: `purple`, `blue`, `pink`, `green`

Available tag classes: `tag-update`, `tag-mod`, `tag-psych`, `tag-community`, `tag-engine`, `tag-mobile`

### Updating the Ticker

Find the `.ticker-track` element and edit the `<span>` texts. The ticker is duplicated — update both halves to keep the seamless loop animation working.

### Adding Search Results

Find the `allContent` array in the `<script>` block and append entries:

```javascript
{ tag: 'MOD', title: 'Your news title here' },
```

---

## CSS Variables

The entire color palette is controlled by CSS custom properties at the top of the stylesheet:

```css
:root {
  --bg: #0a0010;
  --neon-purple: #bf00ff;
  --neon-blue: #00cfff;
  --neon-pink: #ff00aa;
  --neon-yellow: #ffe600;
  --neon-green: #00ff88;
}
```

---

## Category Tags Reference

| Tag Class | Color | Use For |
|---|---|---|
| `tag-update` | `#00ff88` (green) | Engine/library version releases |
| `tag-mod` | `#bf00ff` (purple) | New mods or mod updates |
| `tag-psych` | `#00cfff` (blue) | Psych Engine specific news |
| `tag-community` | `#ff00aa` (pink) | Community events, jams, milestones |
| `tag-engine` | `#ffe600` (yellow) | Engine development and forks |
| `tag-mobile` | `#ff6600` (orange) | Mobile ports and platform support |

---

## Contributing

Pull requests are welcome. To contribute a news post or UI improvement:

1. Fork the repository
2. Create a branch: `git checkout -b feature/your-change`
3. Edit `index.html`
4. Open a pull request with a brief description of what changed

For large structural changes, open an issue first to discuss the approach.

---

## License

Distributed under the **Apache 2.0 License**. See [`LICENSE`](./LICENSE) for full terms.

---

<div align="center">

**Funkin' News** — *Made by the community, for the community.*

Not affiliated with Newgrounds or the official Friday Night Funkin' team.

</div>
