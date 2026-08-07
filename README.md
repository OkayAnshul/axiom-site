# axiom-site

Marketing and documentation site for **Axiom**, an Android journalling app.

Live at **https://okayanshul.github.io/axiom-site/**

## Contents

| File | Purpose |
|---|---|
| `index.html` | Landing page — features, screenshots, engineering notes |
| `privacy.html` | Privacy policy. **This is the URL Google Play Console requires.** |
| `assets/css/style.css` | All styling. Palette lifted from the app's `AxiomColors.kt`. |
| `assets/shots/` | Screenshots, light and dark, straight from a debug build |

## Design

Static HTML and CSS with no build step and no JavaScript, so GitHub Pages serves it directly from
`main`. Everything is self-contained — no CDN, no web fonts, no third-party requests, which keeps
the site consistent with what the app itself claims about tracking.

Light and dark are both handled through `prefers-color-scheme` using the same colour tokens the
app uses, so the site and the product look like one thing.

## Publishing

Settings → Pages → **Deploy from a branch** → `main` / `/ (root)`.

The privacy policy URL must resolve publicly before it can be submitted in Play Console — Google
validates it at submission time.
