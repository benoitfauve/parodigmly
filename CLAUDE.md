# CLAUDE.md: Parodigmly handover

## What this is
A humorous parody landing page for a fictional SaaS product, "Parodigmly". It exaggerates the visual tells of AI-generated (especially Claude-generated) websites. The joke only works if the page itself looks polished: keep the craft high and the content absurd.

Live preview (private claude.ai artifact): https://claude.ai/artifact/WUWeJFv82ohEJVrNqib24C

## Structure
- `index.html`: the whole site in one file: inline CSS, inline JS, no build step, no dependencies apart from Google Fonts (Inter, JetBrains Mono).
- Data-driven sections are arrays in the script block (`lines`, `logos`, `kpis`, `feats`, `steps`, `bars`, `plans`, `msgs`) rendered with `map().join('')`. Edit copy there rather than in the markup.

## Run locally
Open `index.html` in a browser, or `python3 -m http.server` and visit http://localhost:8000.

## The tells being parodied (keep these)
1. Tiny uppercase monospace "eyebrow" labels in green above every heading (`.eyebrow`).
2. Two-colour headings: one or two words in accent green (`.g`; `.g2` turns green only at high Claude-ness).
3. KPI tiles with count-up numbers and a green "up" badge (`#kpis`).
4. Sliding "trusted by" logo bar (`.ticker` / `.track`, CSS marquee duplicated for a seamless loop).
5. Terminal block that types itself (`#term`).
6. Also: "NEW" pill, glow blobs, emoji feature cards, "Three steps. Always three.", MOST POPULAR pricing badge, "Key takeaways" box, gradient progress bars.

## The Claude-ness dial
Fixed control bottom-right (`#vibe`, range 0 to 11). It sets the CSS variable `--v`, which drives eyebrow letter-spacing, glow strength, button glow and ticker speed. At 8+ the body gets `.extra` (more green words). At 0 the body gets `.plain` (everything reverts to Times New Roman on white). At 11 a toast appears.

## Conventions
- Owner's style: neutral, technical wording in docs and commits; avoid em-dashes in commit messages and docs (the em-dash jokes inside the parody copy are deliberate).
- Keep it a single self-contained file unless there is a strong reason to split.
- Respect `prefers-reduced-motion` (already handled for ticker, caret, bars).
- All names, companies and testimonials are fictional. Do not add real brands, logos or real people.

## Possible next steps
- Deploy with GitHub Pages (Settings > Pages > deploy from `main`, root).
- Add an Open Graph image so links on Bluesky show a preview card.
- More gags: cookie banner that is "absolutely right", a changelog with daily major versions, a FAQ where every answer starts with "Great question!".
