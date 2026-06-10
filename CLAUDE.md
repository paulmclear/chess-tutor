# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A personal chess-learning workspace for Paul (~800 on chess.com, goal: 1000 → 1200). It is a **static site with no build step, no dependencies, and no tests** — plain HTML files deployed to Netlify (`netlify.toml`: publish root, empty build command). Open any page directly, e.g. `open lessons/0002-tactics-the-fork.html`.

## Structure & content rules

- **Public site:** `index.html` (landing hub), `lessons/NNNN-*.html`, `reference/*.html`, `404.html`.
- **Private workspace files** (blocked from the public site via 404 redirects in `netlify.toml`): `MISSION.md`, `NOTES.md`, `RESOURCES.md`, `paul-brand-system.html`, `learning-records/`. If a new private file or directory is added, it MUST get a matching redirect rule in `netlify.toml`.
- New lessons: sequential four-digit prefix (`lessons/0003-...html`), then add a lesson card to `index.html` and update any "coming soon" placeholder.
- `learning-records/NNNN-*.md` capture what Paul has demonstrably learned/agreed — append new records, don't rewrite history.

## Teaching context (read before writing any lesson)

`MISSION.md`, `NOTES.md`, and `RESOURCES.md` are the source of truth for *what* to teach and *how*:

- Agreed sequence: tactics/blunder-checking → converting won positions → opening principles → middlegame plans. Memorised opening theory is explicitly out of scope below ~1300.
- Lessons are small (single-sitting, 1–3 hrs/week budget), one concept each, evidence-led with citations drawn from `RESOURCES.md`.
- Paul plays classical time controls — emphasise "what to look for" (checklists, scan habits) over speed or memorisation.

## Design system

Lessons and pages use **Paul's personal brand system** (`paul-brand-system.html` — "Refined Naturalist"), not a company brand; these are personal learning artifacts. Each HTML file is fully self-contained: inline `<style>` with the brand CSS variables copied in (Canopy greens, Birch neutrals, Slate navy, Tortoise + Claude coral accents; Playfair Display / Libre Baskerville / DM Sans / DM Mono via Google Fonts). Copy the `:root` block from an existing lesson when creating a new page.

Chessboard conventions (worked out by trial — reuse, don't reinvent):

- Pieces are SOLID Unicode glyphs (♚♛♜♝♞♟) for both sides, coloured per side with an *outside* stroke via `paint-order:stroke fill`: White = white fill + `-webkit-text-stroke:1.7px #14110d`; Black = dark fill + `1.5px #f0e9db` stroke; plus `drop-shadow(0 1px 1.5px rgba(0,0,0,.4))`. Thin strokes without `paint-order` wash the pieces out.
- Dark squares are Canopy green `#3a7049` (`--sq-dark`).
- Boards scale on mobile with `--sq:calc((100vw - 100px)/8)` inside `@media (max-width:600px)`.
