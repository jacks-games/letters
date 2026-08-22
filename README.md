# ✏️ Jack's Letters

### Write every letter with your finger. ⚽

# [▶ PLAY](https://jacks-games.github.io/letters/)

![Jack's Letters: the letter q, half traced in yellow, with a green dot showing where to start](screenshot.png)

## 🎮 How to play

### 1️⃣ &nbsp; Find the green dot 🟢
Every letter starts in one special place. The little arrow shows which way to go.

### 2️⃣ &nbsp; Slide your finger 👆
Follow the grey line. Do not lift your finger! If you lift it, that line starts again.

### 3️⃣ &nbsp; The line turns green ✅
One line done. Some letters have two or three lines — keep going.

### ⚽ &nbsp; You wrote it!
The letter fills in and you win a football.

## 🔤 26 letters, in the right order to learn them

Not a, b, c — letters that are **written the same way** come together:

| | |
|---|---|
| ⭕ **Round ones** | c &nbsp; a &nbsp; d &nbsp; g &nbsp; o &nbsp; q &nbsp; s &nbsp; e &nbsp; f |
| ⬇️ **Straight down** | i &nbsp; l &nbsp; t &nbsp; u &nbsp; j &nbsp; y |
| 🌉 **Down and over** | r &nbsp; n &nbsp; m &nbsp; h &nbsp; b &nbsp; p &nbsp; k |
| ⚡ **Zig-zag** | v &nbsp; w &nbsp; x &nbsp; z |

Green letters at the top are the ones you have done. Tap any letter to jump to it. 🟩

## 🎯 What you get better at

- ✍️ &nbsp; Starting every letter in the right place
- 🔄 &nbsp; Moving your hand the right way round
- 👀 &nbsp; Seeing how tall each letter is

## 🎈 More games for Jack

[📖 Words](https://github.com/jacks-games/words) · [🥅 Match](https://github.com/jacks-games/match) · [✏️ Letters](https://github.com/jacks-games/letters) · [🔢 Numbers](https://github.com/jacks-games/numbers) · [♟️ Chess](https://github.com/jacks-games/chess)

👉 &nbsp; All of them together: **[jackbenn.ing](https://jackbenn.ing)**

---

<details>
<summary><b>For grown-ups</b> — how the tracing is checked</summary>

Colouring a letter in is not writing it. This checks **formation**: the right start point, the right direction, the right stroke order.

Each lowercase letter is one to three SVG stroke paths in a 100 × 140 box, with ascender, x-height, baseline and descender drawn as faint guides. For every stroke the app samples about twenty checkpoints along the path with `SVGPathElement.getPointAtLength()`; the finger has to reach them **in order**, within a tolerance radius. Passing several at once is fine, so a fast swipe still counts — skipping the middle of the stroke does not. Lifting the finger before the end resets that stroke.

Ink is drawn on a `<canvas>` above the SVG using pointer events with `touch-action: none`, so a finger draws instead of scrolling the page.

`TOL` (17 board units) is the knob to turn if it feels too fussy or too generous for a particular child.

One self-contained `index.html`, no build step, no dependencies, no accounts, no tracking. Progress lives in `localStorage`.

Source of truth for all of Jack's games is the [jackbenn.ing repo](https://github.com/google814/Jack); this repo is a copy so the game has its own page and link.

```bash
python3 -m http.server 8000
```
</details>
