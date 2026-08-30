# Territory Wars

A small turn-based strategy game about capturing territory and crushing the enemy army — built as a single, dependency-free HTML file so it's easy to host, fork, or drop into any repo. Designed mobile-first (tap controls, responsive layout).

Play it locally by opening `index.html` in any browser, or host it for free with GitHub Pages (see below).

## How to play

- You're **blue**, the enemy AI is **red**. Each has a **base** (★).
- Tap one of your units to select it, then tap an adjacent tile to:
  - **Move** into an empty/neutral tile — this captures it for you.
  - **Attack** an enemy unit on an adjacent tile — combat is resolved with a bit of randomness weighted by attack stat; the loser is destroyed.
- Tap your own **base** (when it has no unit standing on it) to recruit a new unit:
  - **Infantry** — cheap, weak (30 gold, 10 HP, 4 ATK)
  - **Tank** — expensive, strong (70 gold, 20 HP, 8 ATK)
- You earn gold each turn based on how many tiles you control.
- Tap **End Turn** once you've moved everything you want to move.
- **Win** by capturing the enemy base or wiping out their entire army. If turn 40 is reached, whoever controls more tiles wins.

## Running it

No build step, no dependencies — it's a single HTML file.

```bash
# just open it directly
open index.html      # macOS
# or
start index.html     # Windows
# or serve it locally
python3 -m http.server 8000
```

## Deploying to GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a branch`, pick your default branch and the `/ (root)` folder.
4. Save — GitHub will give you a live URL (something like `https://<username>.github.io/<repo>/`) within a minute or two.

## Project structure

```
.
├── index.html   # the entire game — HTML, CSS, and JS
├── README.md
└── LICENSE
```

## Possible next steps

- Add more unit types (ranged, cavalry) or terrain (mountains, rivers) that affect movement/combat.
- Add a difficulty setting for the AI.
- Add local two-player hotseat mode.
- Save/load game state with `localStorage`.

## License

MIT — see [LICENSE](LICENSE).
