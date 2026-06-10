# Teaching Notes — Chess

## Learner snapshot
- ~800 on chess.com. Plays **classical / long time controls**. Studies 1–3 hrs/week.
- Goal: climb the rating ladder (milestone: 1000 → 1200).
- Stated interest: "theory, openings, perfect my middle game."

## Key teaching stance
- Paul *asked* for openings/theory/middlegame, but the honest, evidence-backed
  truth is that tactics + blunder-checking dominate results below ~1300. I told him
  this up front and he's on board with a principles-first (not memorisation) path.
  **Honour the interest, but sequence it correctly: tactics → conversion → opening
  principles → middlegame plans.**
- He responds well to "show me why" — keep lessons citation-heavy and evidence-led.

## Lesson design preferences
- Small, single-sitting lessons (1–3 hrs/week budget). One thing per lesson.
- Plays classical, so emphasise *what to look for* over speed/memorisation.
- Deliverables follow **Paul's PERSONAL brand system** (`paul-brand-system.html`),
  NOT Plenitude's. These are personal learning artifacts, not company work.
  Brand = "Refined Naturalist": Canopy greens (primary, #4d8c5e/#2a5736), Birch
  neutrals, Slate navy, Tortoise (#8c5a1e) + Claude coral (#c25840) accents.
  Fonts: Playfair Display (display), Libre Baskerville (body prose), DM Sans (UI),
  DM Mono (labels/code). Boards use a Canopy-green dark square (#3a7049) to fit.
- **Chessboard piece rendering (reuse this — verified legible on light & dark squares):**
  All pieces use the SOLID Unicode glyphs (♚♛♜♝♞♟); colour them per side and outline with
  `paint-order:stroke fill` so the stroke sits OUTSIDE the fill. White = white fill +
  dark outline (`-webkit-text-stroke:1.7px #14110d`); Black = dark fill + cream outline
  (`1.5px #f0e9db`); plus `drop-shadow(0 1px 1.5px rgba(0,0,0,.4))`. The first attempt
  (thin outline, no paint-order) washed pieces out — Paul flagged it; this is the fix.
- Boards scale on mobile via `--sq:calc((100vw - 100px)/8)` inside a `@media (max-width:600px)`.
- Lessons should open with one CLI command (`open lessons/NNNN-*.html`).

## Open questions / to revisit
- Confirm whether Paul wants to join a community (r/chessbeginners) for game reviews.
- Get a real game of his to analyse once habits are introduced — grounds everything.
- Pick an endgame video + an opening repertoire source when we reach those stages.
