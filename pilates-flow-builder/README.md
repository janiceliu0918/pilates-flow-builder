# Pilates Class Flow Builder

An open, browser-based tool that helps Pilates instructors design class sequences
with smooth transitions, level-appropriate choices, prop options, and
special-population safety flags — so they can spend their prep time on personal
cueing instead of logistics.

**Live demo:** _enable GitHub Pages (see below), then link it here_
`https://<your-username>.github.io/pilates-flow-builder/`

## What it does

- **Flow-aware sequencing.** Pick an exercise and the list re-sorts to the moves
  that flow smoothly from it. Transitions are scored automatically:
  - 🟢 **Seamless** – same apparatus, position, spring, and facing
  - 🟠 **Minor** – same apparatus, one change (spring / position / facing)
  - 🔴 **Major** – change of apparatus
- **Reordering.** Drag (⠿) or use ▲▼; transitions recompute live.
- **Click-to-view.** Click any step to inspect it up top; new moves insert after it.
- **Back-and-forth guard.** Groups work by station and warns if you leave and
  return to an apparatus — or to a reformer **short box / long box / jumpboard**
  setup (each should be set up only once).
- **Levels & props.** Filter by level (1.0 / 1.5 / 2.0), apparatus, and prop
  (magic circle, band, small ball, weights, TRX, Bosu, block) with placement cues.
- **Special-population mode.** Choose a client condition and every exercise is
  flagged **Safe / Caution / Avoid** from its movement profile, with avoid /
  utilize / programming guidance.
- **Print / Save-PDF** the finished sequence.

## Data model

Everything is data-driven — no code changes needed to grow the library.

- `data/exercises.json` — the exercise library. Each entry carries apparatus,
  level, spinal position, orientation, spring setting, movement type(s), cues,
  optional props (with cues), and (for reformer) its station setup.
- `data/special_populations.json` — condition definitions with avoid / caution
  movement + position rules, plus guidance text.

The app ships with this data embedded, so `index.html` runs on its own with no
build step and no server.

## Run locally

Just open `index.html` in any browser. That's it.

## Deploy on GitHub Pages

1. Push this repo to GitHub (see below).
2. Repo **Settings → Pages**.
3. Under *Build and deployment*, set **Source: Deploy from a branch**,
   **Branch: `main` / `/root`**, then **Save**.
4. Wait ~1 minute; your tool is live at
   `https://<your-username>.github.io/pilates-flow-builder/`.

## Roadmap ideas

- Expand the apparatus repertoire and add more special-population conditions.
- Save / load and share sequences via a link.
- Instructor accounts and a class library.

## Disclaimer

This tool is educational and is **not medical advice**. The special-population
guidance reflects widely accepted Pilates and rehabilitation movement-safety
principles. Clients with any medical condition should have physician or
physiotherapist clearance, and the instructor's professional judgment governs
all programming.

## License

Code released under the [MIT License](LICENSE) © 2026 Kaiyi (Janice) Liu.
