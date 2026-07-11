# Rebrand: ₿uilder SF → Builders Turin

This document records the rebrand of this repository to a single, consistent brand:
**`Builders Turin`** — the Turin chapter of the Bitcoin Builder network, served at
**https://bitcoinbuilderturin.xyz**.

## Why

The repository previously carried a split identity: the GitHub repo was named
`BitcoinBuilderTurin`, but all site content and templates were branded `₿uilder SF`
(San Francisco), with an SF custom domain and SF community links. This rebrand
consolidates everything to **one brand (`Builders Turin`)** in **one repository**, keeping the
multi-city "Cities" page so Builders Turin remains part of the wider Bitcoin Builder network.

## Decisions

- **Brand / display name:** `Builders Turin`.
- **Identity model:** Turin *chapter* — the multi-city "Cities" structure is kept; Turin
  is added alongside the existing SF / Austin / Miami / Vancouver chapters.
- **Domain:** `bitcoinbuilderturin.xyz`.
- **Historical event posts** (`content/builder-01.md` … `builder-07.md`): archived as-is.
  Only the post *titles* were renamed (`₿uilder N` → `Builders Turin N`); bodies (which recap past
  SF events at Presidio Bitcoin) are preserved as a historical record.

## Changes applied

| File | Change |
|---|---|
| `config.toml` | `base_url` → `https://bitcoinbuilderturin.xyz`; added `title = "Builders Turin"` and `description` (both are consumed by `templates/feed.xml` and were previously unset, so the RSS feed title/subtitle rendered empty). Also removed the obsolete `[markdown] highlight_code = false` field — see "Incidental fix" below. |
| `CNAME` | `www.bitcoinbuildersf.com` → `bitcoinbuilderturin.xyz`. |
| `static/CNAME` | **Deleted** — redundant duplicate of the root `CNAME` and contained a typo (`wwww.…`). The root `CNAME` is the single source of truth (CI copies it into `public/`). |
| `templates/base.html` | `<title>`, `<h1>`, `meta description`, `meta author` rebranded to `Builders Turin`; GitHub nav link → `github.com/dev-crew-it/BitcoinBuilderTurin`. |
| `templates/index.html` | Intro paragraph and logo `alt` rebranded to `Builders Turin`. |
| `README.md` | Rewritten for Builders Turin / Bitcoin Builder Turin; added a Development section. |
| `content/cities/_index.md` | Added Turin to the chapter list. |
| `content/builder-0{1..7}.md` | Post titles renamed `₿uilder N` → `Builders Turin N`. |

## Outstanding TODOs (marked `TODO(rebrand)` in the code)

These need real values before deploy; placeholders are in place so the site still builds:

- **Turin Meetup group URL** — `templates/base.html` (Meetup nav link).
- **Turin Twitter/X handle** — `templates/base.html` nav link and `README.md`.
- **BitDevs / LitDevs** — `templates/base.html` still points at the SF orgs
  (`sfbitcoindevs.org`, `sflightningdevs.org`); point to Turin equivalents or remove.
- **Voting organization link** — `templates/base.html` (was the SF org id).
- **Logo** — `templates/index.html` still uses the SF org's GitHub avatar; replace with a
  Builders Turin logo (drop a file in `static/` and reference it).
- **Venue / cadence** — `README.md` (was "Presidio Bitcoin", the SF venue).

## Incidental fix (required for the build to pass)

The pre-existing `[markdown] highlight_code = false` field in `config.toml` is no longer a
valid option in current Zola (tested with 0.22.1, which is what the CI's `brew install zola`
installs). It caused `zola build` to fail before this rebrand too, so the deploy was already
broken. The field was removed (code highlighting is off by default), which unblocks the build.

## Deployment

GitHub Pages is published via the **official GitHub Actions flow**
(`actions/upload-pages-artifact` + `actions/deploy-pages`), replacing the previous
third-party `peaceiris/actions-gh-pages` deploy that pushed to a `gh-pages` branch.
Pages is configured with **build type = GitHub Actions** (no `gh-pages` branch needed).
The custom domain `bitcoinbuilderturin.xyz` is set via the root `CNAME`, which the build
job copies into `public/` before uploading the artifact.

There were no pre-existing Pages deployments, environments, or `gh-pages` branch on this
repo to remove — Pages had never been enabled here.

## Verify

```sh
just serve        # local preview (zola serve --drafts)
just check-links  # internal link check
zola build        # builds into public/
```

CI (`.github/workflows/ci.yaml`) runs the build + link check and deploys to GitHub Pages
on `main`; the root `CNAME` is copied into `public/` during deploy. No CI changes required.
