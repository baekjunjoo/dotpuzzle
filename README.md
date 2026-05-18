# DotPuzzle Pack — Daily Tactile Puzzles for Dot Pad

4-in-1 puzzle game prototype designed for the Dot Pad multi-line tactile display. Grid puzzles = perfect tactile mapping. One Pad cell = one puzzle cell.

## What's inside

| Puzzle | Size | Dot Pad mapping |
|---|---|---|
| **Sudoku** | 9 × 9 | Digit → dot count (1 dot = 1, 2 dots = 2, ...). Cursor = bracket pattern. |
| **Minesweeper** | 9 × 9 | Revealed number → dot count. Mine = all 6 dots. Flag = dots 2+5. Hidden = dots 1+4. |
| **Nonogram** | 10 × 10 | Filled = all 6 dots. X mark = dots 2+5. Hints in side panels. |
| **Maze** | 15 × 15 | Wall = solid block. Goal = small marker. Player = blob. Viewport scrolls with player. |

## How to play (no Dot Pad)

- Open `index.html` in Chrome or Edge.
- Click puzzle cards to start.
- Mouse / arrow keys / on-screen number pad work everywhere.
- The **DOT PAD PREVIEW** strip at the bottom of each puzzle simulates the tactile output for the current row.

## How to play (with Dot Pad)

1. Open in **Chrome / Edge desktop**.
2. Serve over HTTPS (GitHub Pages works, or `python -m http.server` + ngrok).
3. Click **Pad** in the header → connect via Bluetooth or USB.
4. Key map (same on every screen):
   - **F1** prev row · **F2** next row
   - **Pan Left** prev column · **Pan Right** next column
   - **F3** select / cycle digit
   - **F4** toggle flag / X mark / check
   - **Pan All** replay current state via voice

## Voice

Web Speech API (browser-native). No API keys needed. Cell location + state announced on every cursor move. Toggle off with the **VOX** button.

## Files

```
dotpuzzle-prototype/
├── index.html          # all 4 puzzles in one file
├── dotpad-sdk/
│   └── DotPadSDK-3.0.0.js
└── README.md
```

## Deploy to GitHub Pages

```bash
cd ~/Documents/Claude/Projects/Dot\ Arcade/dotpuzzle-prototype
git init
git add .
git commit -m "DotPuzzle Pack v0.1 — 4 puzzles + Dot Pad integration"
git branch -M main
# Create empty repo at github.com/<you>/dotpuzzle first, then:
git remote add origin https://github.com/<you>/dotpuzzle.git
git push -u origin main
```

In the repo settings → **Pages** → branch `main` → root → save. After a minute the demo will be at `https://<you>.github.io/dotpuzzle/`.

## What's next

- AI-generated puzzles (Sudoku/Nonogram/Maze procedural generation, Claude API for hint generation)
- Difficulty levels
- Daily challenge mode (one shared seed per day)
- Echo Lake-style Dot Pad ambient sound on cell change
- Internationalization (Korean voice + braille labels)
- Stats / streaks

## License

Internal prototype — Dot Inc.
