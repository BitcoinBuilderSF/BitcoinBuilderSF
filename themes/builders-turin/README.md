# builders-turin (Zola theme)

Retro pixel/terminal theme for a Bitcoin builders meetup. Bundles the
Press Start 2P + VT323 fonts (self-hosted, no external requests) and ships a
default social preview image (og-image.jpg).

## Install
1. Add the theme to your Zola site, e.g. as a submodule:
   git submodule add <repo-url> themes/builders-turin
   (or copy this directory into themes/builders-turin)
2. In config.toml set: theme = "builders-turin"
3. Provide your own content/ and set title, description, base_url in config.toml.

## Customize
- Override any template by adding templates/<name>.html in your site
  (site templates take precedence over the theme).
- Replace the preview image by adding static/og-image.jpg in your site
  (site static overrides theme static).
- Fonts are bundled under static/fonts/ (no third-party font requests).

## Notes
- Branding strings (nav links, community handles, hero/footer copy) currently
  live in the templates. To rebrand, edit or override the templates (an
  [extra] config pass can externalize them in a follow-up).
- Licensed CC0-1.0 (same as the site).
