---
name: Skull King Scoring App
description: Single-file HTML scoring companion for the Skull King card game, published to GitHub Pages
type: project
---

Single-file app at `index.html` (no build step). Published via GitHub Pages at the repo root.

**Tech:** Vanilla HTML/CSS/JS, Google Fonts (Pirata One + Cinzel), localStorage key `skull_king_v1`.

**Features built:**
- Setup: 2–8 players, add/delete, Skull King's vs Rascal's scoring system toggle, Advanced Rules toggle
- Game: swipeable player carousel (touch), round nav (< >), scoreboard modal, new game button
- Per-player card: bid stepper, tricks stepper, cannonball/grapeshot toggle (Rascal+advanced), bonus stepper (±10, can go negative), live bid status badge, round score + running total
- Bonus reference modal with all bonus values
- Game over: ranked final standings with medals
- localStorage persistence + new game confirmation modal

**Scoring logic (exact):**
- Skull King's: bid 0 correct = +10×cards; bid 0 wrong = -10×cards; bid N correct = +20×N; bid N wrong = -10×|diff|. Bonus only if exact.
- Rascal's Grapeshot: mult = 1/0.5/0 for diff 0/1/2+. Points = round(10×cards×mult + bonus×mult).
- Rascal's Cannonball (advanced): correct = 15×cards + bonus; wrong = 0.

**Why:** User (Jacob) plays Skull King with 5–7 people and wanted a mobile-optimized iPhone scorekeeper to replace paper scoresheets.

**How to apply:** If asked to modify the app, edit `index.html` directly. No build step needed. Keep all code in the single file.
