# SQL Asteroids

A browser-based arcade game that teaches SQL through gameplay. Destroy asteroids, get quizzed on SQL concepts, and level up your database knowledge — all in a retro 90s arcade aesthetic.

**[▶ Play Now](https://isokimmy.github.io/sql-asteroids/)**

---

## How to Play

| Key | Action |
|-----|--------|
| `← →` | Rotate ship |
| `↑` | Thrust forward |
| `Space` | Fire cannon |

- Destroy **10 × level** asteroids to trigger a SQL quiz
- Answer correctly → **advance to the next level**
- Get hit by an asteroid → SQL quiz
- Answer correctly → **recover your lost life**
- Wrong answer? No benefit — keep fighting
- You have **3 lives**. Don't waste them.

---

## SQL Topics by Level

| Level | Topics |
|-------|--------|
| 1 | `SELECT`, `WHERE`, `ORDER BY`, `DISTINCT`, `LIMIT` |
| 2 | `INNER JOIN`, `LEFT JOIN`, `FULL OUTER JOIN`, `GROUP BY`, `HAVING`, aggregate functions |
| 3 | Subqueries, `EXISTS`, `COALESCE`, `IS NULL`, aliases |
| 4 | Window functions (`ROW_NUMBER`, `RANK`, `DENSE_RANK`, `LAG`, `SUM OVER`), CTEs (`WITH`) |

Each level's questions get progressively harder. Destroy more asteroids per level as difficulty increases.

---

## Visual Themes

Switch themes on the start screen — the live background previews instantly.

| Theme | Palette |
|-------|---------|
| Deep Space | Purple / Cyan / Magenta |
| Acid Neon | Matrix green / Lime / Teal |
| Solar Storm | Orange / Red / Gold |
| Synthwave | Hot pink / Violet / Electric blue |
| Ghost | Ice white / Silver / Pale blue |

---

## Features

- **Real-time physics** — thrust, friction, momentum, screen wrapping
- **Asteroid splitting** — large → medium → small before fully destroyed
- **25 SQL questions** across 4 difficulty tiers
- **Adaptive quiz system** — question difficulty scales with level, no repeats until the pool is exhausted
- **5 swappable visual themes** — affects nebulae, asteroids, ship, bullets, HUD, and particles
- **Procedural background** — animated nebula gradients, 3-tier twinkling starfield, CRT scanline overlay
- **Zero dependencies** — single HTML + JS, open in any browser

---

## Running Locally

No build step needed. Just open the file:

```bash
git clone https://github.com/isokimmy/sql-asteroids.git
cd sql-asteroids
# Open sql-asteroids.html in your browser
```

Or use a local server to avoid any file:// restrictions:

```bash
npx serve .
# or
python -m http.server 8000
```

---

## Project Structure

```
sql-asteroids/
├── sql-asteroids.html   # Markup and styles
└── sql-asteroids.js     # Game engine, themes, and SQL question bank
```

---

## Tech Stack

- **Vanilla JavaScript** — game loop, physics, collision detection, rendering
- **Canvas 2D API** — all game graphics drawn programmatically (no sprites)
- **HTML/CSS** — start screen UI, quiz overlay, theme selector
