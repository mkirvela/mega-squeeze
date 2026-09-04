# Mega Squeeze

A cold-pressed juice empire in one HTML file. Squeeze the fruit, fill the glass,
buy help, never stop.

It's a clicker — tap to earn, spend on per-tap upgrades and passive presses,
climb ranks, replant for a permanent multiplier. The point of the exercise was
game feel, so every system is built to be felt:

- **Jelly fruit** — spring physics; it squashes on press, pokes away from where
  your finger landed, and wobbles back with overshoot.
- **The glass is the rank meter.** Each squeeze fires a ballistic pour solved to
  land in the mouth. The surface is a 1-D spring water sim, so every drop lands
  with a ripple that propagates and reflects off the walls. Fill it and it's
  **SERVED** — the glass drains and a bigger fruit arrives.
- **Frenzy** — mash fast for ×2/×3/×5/×8, with rising pitch, growing shake and a
  vignette that heats with the combo.
- **Golden Squeeze** — crits at ×10, with a white flash, sparks and a shockwave.
- **Eight fruit tiers**, hand-built as SVG: lemon segments, orange pith,
  pomegranate seeds, watermelon stripes, dragonfruit scales, a starfield fig,
  and haloed Ambrosia. The whole palette retints per tier.
- **Lifetime spill** along the bottom edge that grows with total squeezes and
  never gets cleaned up.

Squeezes are lifetime — they survive replanting.

## Running it

Open `index.html`. That's it: no build, no dependencies, no bundler. The only
network request is the Google Fonts stylesheet, and it falls back cleanly
offline.

To play on a phone on the same Wi-Fi:

```sh
python3 -m http.server 8000
```

Then open `http://<your-lan-ip>:8000` and add it to your home screen — it runs
fullscreen. On small screens the press room collapses into a bottom sheet so
nothing sits on top of the play area, and tapping anywhere in the stage counts.

Progress autosaves to `localStorage`, including offline earnings (capped at two
hours).

`prefers-reduced-motion` is respected throughout.
