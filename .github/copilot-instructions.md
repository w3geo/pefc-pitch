# Copilot Instructions

This is a [Slidev](https://sli.dev) presentation project for a pitch to PEFC.

## Presentation

- **Title:** PEFC-EUDR-RED Datenbankapplikation
- **Language:** German
- **Theme:** `seriph`
- **Transition:** `fade-out` (global)
- **Duration:** 15 min

## Static Assets

Assets are split into two directories depending on how they are used:

- **`assets/`** — images embedded in slide content via `<img>` or markdown. These go through Vite's markdown processing pipeline. Reference them as `./assets/my-image.png`.
- **`public/`** — slide backgrounds set via the `background:` frontmatter key. These do **not** go through markdown processing and must be served as static files. Reference them as `./my-background.webp` (no `public/` prefix, no `assets/` prefix).

Do **not** use absolute paths like `/filename` in `<img src>` attributes — those trigger Vite's import guard.

Current assets:
- `public/background.webp` — forest background (title slide, referenced as `./background.webp` in frontmatter)
- `assets/w3geo-logo.png` — presenter company logo (bottom-right, title slide, `brightness(3)` filter)
- `assets/pefc-logo.png` — addressee logo (bottom-left, title slide)

## Title Slide Conventions

- Logos placed with `abs-br` / `abs-bl` and `m-8 h-12` classes
- Background set via `background:` in frontmatter

## Slide Structure

Section divider slides use `layout: section`. Sub-topic slides are plain.

Content slides use **bullet points** as the primary content format. Images go below the bullet points (or replace them if a visual is more effective). Keep slides concise — a few bullets per slide.

Example (EUDR slide):

```md
# EUDR

- Bereits Erfahrung mit EUDR durch Entwicklung des **BMLUK EUDR-Meldung**-Tools
- Kenntnis der Prozesse rund um EUDR-Sorgfaltserklärungen und Referenznummern
- Technisches Know-how zur Anbindung an die **TRACES**-Datenbank

<!-- AH -->
```

Every slide has a presenter note (`<!-- AP -->` or `<!-- AH -->`) indicating which presenter delivers it:
- **AP** — Allgemeiner Intro section (Thema: BML/Wald, Datenbank/Design, Serverlandschaften/Hosting, soFisch/Istmobil) and Web-Formulare
- **AH** — Authentifizierung, EUDR, Duplikatvermeidung und mehr, Altdaten-Übernahme slides

## Icons

Slidev uses [unplugin-icons](https://github.com/antfu/unplugin-icons). Icons are used as **Vue components** — NOT as UnoCSS `i-*` classes.

Format: `<{collection}-{icon-name} class="..." />`

Installed icon sets: `@iconify-json/carbon`, `@iconify-json/ph` (Phosphor), `@iconify-json/svg-spinners`

Examples:
```md
<ph-flashlight class="text-6xl text-amber-300 mx-auto block" />
<carbon-flash class="text-4xl text-yellow-400" />
```

Browse available icons at https://icones.js.org/
