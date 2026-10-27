# Queer Gambit

A chess clock that runs in the browser, on a phone lying next to the board. The chess version
of the Go Girls* Timer (`../go-timer`), made because more people play chess.
Built by Sina with Claude, October 2026. *A Go Girls\* App by Sina.*

Live at **https://sinalaura.github.io/chess-timer** (repo `SinaLaura/chess-timer`, GitHub Pages
from `main`, `/ (root)`). Every push goes live by itself.

## What it does

- Two big halves of the screen, one per player. White moves first: tap Black's half to start
  White's clock. After your move, tap your own half.
- Two time systems: **Increment (Fischer)**, a main time plus seconds after every move
  (default: Rapid 15 min + 10 s), and a **simple timer**, just a main time.
- A play button before the game; pause (also when you leave the app) with resume, end game
  and adjust time sliding out in the middle; warnings under 1 minute and 10 seconds, a voice
  that says who lost on time, statistics with a chart of the time per move (moves counted in
  pairs, as in chess).
- English and German; the screen stays on during a game; works offline once loaded.
- Easter egg: tap the heart on the running clock for colour themes (Go Girls*, wlw, Trans,
  Pride).

## How it is built

- **One file:** `index.html`, with the HTML, CSS and JavaScript in it. No framework, no build
  step, no server, no login. It opens by double-clicking it.
- Time is measured from the real clock (`performance.now()`), not by counting timer ticks.
- `manifest.webmanifest` and the icon files make it installable as an app; `sw.js` keeps an
  offline copy.
- Most of the code is shared with the Go timer. Last upgraded from it on 27 Oct 2026, up to
  its commit `3610136` (the chess copy was first taken from the Go timer's state of 9 Oct,
  commit `ccc4d69`). To upgrade again, diff the Go timer's `index.html` from `3610136` on,
  and leave out what is Go-only: byo-yomi, the expected game length with board size, the
  Play Store bits.

## Working together

- **Sina** (she/her) builds this, with Claude doing most of the typing. Keep explanations
  short. Show the result: open `index.html` in the browser after each change.
- Small steps: one change at a time, test it in the browser, then commit with a short message.
- Commit and push only after Sina's go-ahead.
- Personal notes, tasks and ideas do not belong here; they live in Sina's `Life` folder.
