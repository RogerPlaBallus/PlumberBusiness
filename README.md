# Cedar & Copper Plumbing Co. — single-page demo

- Fictional plumbing business. 
- Made with **DeepSeek 4.1 Flash** (DeepSeek).
- Made by **Roger Pla Ballús**.

## Stack used

- HTML5, English, one file: `index.html`.
- CSS inline in one `<style>`: custom properties, `grid`/`flex`, light-only palette.
- JavaScript vanilla, ~35 lines inline. No framework, no CDN, no Tailwind, no build, no cookies, no analytics, no network requests after load.
- Graphics: inline SVG symbol sprite + one inline SVG figure. No image files, no icon font.
- Fonts: system UI stack (`ui-sans-serif`, `-apple-system`, `Segoe UI`, Roboto, Helvetica) — zero font downloads.

## Architecture

- None. Static file, no server, no state, no router (in-page anchors).
- JS does one job: maps the fixed weekly hours to an open/closed string.

## Most important aspects

- Efficiency: 0 external requests; every icon is a `<symbol>` reused via `<use>`; native `<details>` instead of an accordion script.
- Light palette only: `color-scheme: light`, off-white background, blue + copper accents, no gradients, no glow, no shadows.
- Bullet-first copy, no invented testimonials or stock photos; the footer states the business is fictional.
- A11y: landmarks, skip link, visible focus rings, AA contrast, `aria-label` on the figure, no motion.
- Safety content: shut-off, drain and power-down steps before the plumber arrives.
- Tests: `index.html?test=1` runs 7 schedule cases (Mon 9:00 / 6:30 / 17:59 / 18:00, Sat 10:00 / 14:00, Sun) and prints PASS/FAIL plus the console log.

## Install / download

- Download `index.html` and open it in a browser.
- Optional local server: `python3 -m http.server` → http://localhost:8000
- Self-test: `index.html?test=1`
- Deploy: drop the file on any static host (GitHub Pages, Netlify, any web folder).

## Known ceilings

- Hours are hardcoded and use the visitor's local clock, no timezone handling (marked `ponytail:` in code). Expand if non-US visitors matter.
- Contact is `tel:` / `mailto:` only; no booking form because there is no backend.
- Rates table is illustrative, not a pricing engine.
