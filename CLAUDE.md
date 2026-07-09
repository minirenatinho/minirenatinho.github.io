# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal EPK (Electronic Press Kit) and portfolio website for Mini Renatinho — musician, game developer, and software developer. Deployed via GitHub Pages (repo `minirenatinho.github.io`) on the custom domain `minirenatinho.com.br` (set by the `CNAME` file). Public URLs in metadata (`canonical`, `og:url`, `sitemap.xml`, etc.) use the custom domain.

## Stack

Vanilla HTML and CSS — no site JavaScript, no build system, no package manager, no compilation step. The site is served exactly as-is. The only scripts are third-party: GoatCounter analytics (`gc.zgo.at`, dashboard at `minirenatinho.goatcounter.com`) and the SoundCloud embed players.

To preview locally, open `index.html` directly in a browser or use any static file server:

```
npx serve .
# or
python -m http.server 8000
```

## Architecture

Single-page site (`index.html`) with a fixed navigation bar linking to in-page sections: Músicas (Music), Jogos (Games), Dev, Sobre (About), and Contato (Contact).

- **`main.css`** — all styling; dark theme with gold (`#f5c542`) accent color throughout
- **`404.html`** — custom not-found page served by GitHub Pages
- **`robots.txt` / `sitemap.xml`** — SEO; update `sitemap.xml`'s `lastmod` on significant content changes
- **`images/`** — photos and icons used in the page (large photos are resized/compressed for web before committing)
- **`pdf/`** — documents (resume/CV, linked from the Sobre section)

The music section embeds SoundCloud iframes. The games section links out to hosted games and downloads. The dev section links to GitHub repos.

## Planned Work

`BACKLOG.md` tracks planned improvements — check it before adding new features to avoid duplicating planned work or contradicting intended direction.

## Adding Games

New games are placed in a subfolder (e.g., `bruxinha-nautica/`) and linked from the games section in `index.html`. The `bruxinha-nautica/` folder contains a Java desktop game as a zip download.
