# 🎮 Bayhaqy Arcade

A handcrafted collection of seven browser mini-games — built with vanilla HTML5 Canvas, Web Audio API, and `localStorage`. No frameworks, no build step, no ads, no installs. Just open and play.

**Live portal:** <https://bayhaqy.github.io/games/>

---

## 🕹️ The Games

| # | Game | Genre | Levels | Highlights |
|---|------|-------|:------:|------------|
| 1 | 🐦 [Angry Birds](./angry-birds/) | Action | 5 | Slingshot physics, wood/stone obstacles, destructible structures |
| 2 | 🧱 [Tetris](./tetris/) | Puzzle | 10 | SRS rotation, hold piece, ghost piece, next-3 preview, varied objectives |
| 3 | 🐤 [Flappy Bird](./flappy-bird/) | Reflex | 10 | Moving & oscillating pipes, rainbow bird palettes per level |
| 4 | 🔢 [2048](./2048/) | Puzzle | 10 | Smooth tile animations, goal-based progression (128 → 65536) |
| 5 | 🏗️ [Stack Tower](./stack-tower/) | Hypercasual | 10 | Perfect-drop width preservation, rainbow blocks, speed ramp |
| 6 | 🌈 [Color Switch](./color-switch/) | Reflex | 10 | Rotating & moving obstacles, color-switch mechanics |
| 7 | 🔄 [Gravity Flip](./gravity-flip/) | Hypercasual | 10 | **Novel mechanic** — tap to flip gravity, coins, per-level palettes |

Each game has:
- 📈 Progressive difficulty across 5–10 hand-tuned levels
- ⭐ Star ratings (1–3 stars per level) based on score / objective
- 💾 Persistent progress saved to `localStorage` (resume where you left off)
- 🔊 Web Audio API sound effects (with mute toggle)
- 📱 Touch + keyboard + mouse support, responsive from 320px to ultrawide
- 🌗 Light / dark theme toggle (defaults to light, remembered per browser)

---

## 🎯 Design Principles

1. **Single-file per game** — each `index.html` is fully self-contained (HTML + CSS + JS). No external dependencies, no CDN required. Drop the folder anywhere and it works.
2. **Mobile-first, desktop-comfortable** — on wide screens the playfield is constrained to a portrait/landscape max-width and centered, so the game feels like a mobile arcade cabinet rather than a stretched canvas.
3. **No build step** — what you read in source is what runs in the browser. Easy to inspect, learn from, or fork.
4. **Progressive level systems** — every game has clear level objectives, star ratings, and unlock progression. A level picker lets you replay any unlocked level.
5. **Accessible audio** — Web Audio API generates all SFX procedurally (no audio files). Mute is one tap away and persists across sessions.

---

## 🚀 Play

Open the portal in any modern browser:

> <https://bayhaqy.github.io/games/>

Pick a game from the grid. Your progress saves automatically. To reset progress for a specific game, open the game and use the in-game reset button (usually in the level picker overlay), or clear `localStorage` for the site.

---

## 🛠️ Tech Stack

- **HTML5 Canvas 2D** — all rendering
- **Vanilla JavaScript (ES2020)** — no frameworks, no transpilation
- **CSS custom properties** — theming via `[data-theme="light|dark"]`
- **Web Audio API** — procedural SFX (oscillators + envelopes)
- **localStorage** — per-game progress persistence
- **`devicePixelRatio` scaling** — crisp rendering on Retina / HiDPI screens
- **`.nojekyll`** — bypasses Jekyll on GitHub Pages so raw files are served as-is

---

## 📁 Repository Structure

```
games/
├── index.html              # Portal page (catalog, filters, animated previews)
├── README.md               # This file
├── .nojekyll               # Bypass Jekyll processing on GitHub Pages
├── angry-birds/
│   └── index.html          # Self-contained game
├── tetris/
│   └── index.html
├── flappy-bird/
│   └── index.html
├── 2048/
│   └── index.html
├── stack-tower/
│   └── index.html
├── color-switch/
│   └── index.html
└── gravity-flip/
    └── index.html
```

---

## 🌐 Deployment

This repo is published via **GitHub Pages** from the `main` branch root. Any push to `main` goes live within ~30 seconds at <https://bayhaqy.github.io/games/>.

To run locally, just open `index.html` in a browser — no server required. (Some browsers restrict `localStorage` on `file://` for certain operations; if you hit that, use `python -m http.server` from the repo root.)

---

## 📝 License & Attribution

Code is written by **Achmad Bayhaqy** as a personal arcade project. Game concepts (Tetris, Flappy Bird, 2048, Angry Birds, Color Switch, Stack Tower) are inspired by classic titles; **Gravity Flip** is an original mechanic. All implementations here are written from scratch and do not use any copyrighted assets.

---

## 🔗 More

- **Portfolio:** <https://bayhaqy.github.io/>
- **GitHub:** <https://github.com/bayhaqy>
- **Blog:** <https://blog.bayhaqy.my.id>

© 2026 Achmad Bayhaqy. Built with HTML5 Canvas.
