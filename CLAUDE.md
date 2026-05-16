# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal EPK (Electronic Press Kit) and portfolio website for Mini Renatinho — musician, game developer, and software developer. Deployed via GitHub Pages at `minirenatinho.github.io`.

## Stack

Vanilla HTML, CSS, and JavaScript — no build system, no package manager, no compilation step. The site is served exactly as-is.

To preview locally, open `index.html` directly in a browser or use any static file server:

```
npx serve .
# or
python -m http.server 8000
```

## Architecture

Single-page site (`index.html`) with a fixed navigation bar linking to in-page sections: Músicas (Music), Jogos (Games), Dev, and Contato (Contact).

- **`main.css`** — all styling; dark theme with gold (`#c9a227`) accent color throughout
- **`main.js`** — minimal JS; handles the games/projects filter tabs (All / Games / Dev)
- **`images/`** — photos and icons used in the page
- **`downloads/`** — audio files (mp3) served directly
- **`pdf/`** — documents (resume/CV)

The music section embeds SoundCloud iframes. The games section links out to hosted games (e.g., Arena Jerimum on itch.io). The dev section links to GitHub repos using card components that are filtered by `main.js`.

## Planned Work

`BACKLOG.md` tracks planned improvements — check it before adding new features to avoid duplicating planned work or contradicting intended direction.

## Adding Games

New games are placed in a subfolder (e.g., `bruxinha-nautica/`) and linked from the games section in `index.html`. The `bruxinha-nautica/` folder (currently untracked) contains a Java desktop game as a zip download.
