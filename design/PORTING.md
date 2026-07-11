# Porting the Builders Turin design into the site

This design/ directory archives the Claude Design handoff for the Builders
Turin (Bitcoin Builder Turin) redesign. It is REFERENCE material only. The
live site is built with Zola (Tera templates + Markdown in content/, styles
in static/index.css).

## Primary design
- project/Builder Torino - Interactive.dc.html — the main design to
  reproduce. Read it top to bottom. It imports project/support.js (the
  DesignCapture runtime, used only by the prototype).

## What to port (and what NOT to)
- Recreate the VISUAL design (layout, type, colors, spacing, the retro
  pixel/terminal aesthetic; fonts "Press Start 2P" + "VT323") in the Zola
  site: templates/base.html, templates/index.html, templates/page.html,
  static/index.css, and config.toml (font links).
- Do NOT ship support.js — it is the prototype interactivity runtime, not
  production code. Reproduce only the UI/visuals.
- Keep the site functional: "zola build" must pass and ./bin/check-links must
  pass. The Turin event at content/builder-01.md must still render.

## Current site shape
- Single event: content/builder-01.md (Builders Turin 1, 2026-07-11).
- Section index: content/_index.md; templates in templates/.
- Brand name is currently "Builders Turin" (the live Luma event is "Bitcoin
  Builder Torino" — confirm before locking copy).

## Don't
- Do not edit files under design/ — it is the source of truth for the look.
- Do not render/screenshot the prototype; the HTML/CSS has everything needed.
