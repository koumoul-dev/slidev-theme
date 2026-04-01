# slidev-theme-koumoul

Koumoul organization theme for [Slidev](https://sli.dev/).

[Live demo](https://koumoul-dev.github.io/slidev-theme/)

## Installation

```bash
npm i slidev-theme-koumoul
```

## Usage

Add the theme to your slide's frontmatter:

```markdown
---
theme: koumoul
---

# My Presentation

Content goes here
```

### Single file mode

Create a `slides.md` file and run Slidev directly:

```bash
npx @slidev/cli slides.md
```

### Local development

To develop or preview the theme, clone this repo and run:

```bash
npx @slidev/cli example.md
```

## Layouts

| Layout | Description |
|--------|-------------|
| `default` | Standard content slide |
| `cover` | Title slide with Koumoul logo |
| `section` | Section divider with blue background |
| `center` | Vertically and horizontally centered content |
| `two-cols` | Two-column layout (use `::right::` separator) |

## Components

### `<KoumoulLogo />`

Displays the Koumoul logo. Auto-imported, usable in any slide.

```markdown
---

# My Slide

<KoumoulLogo />
```

## Brand Colors

| Color | Hex | Usage |
|-------|-----|-------|
| Primary | `#1976D2` | Headings, links, accents |
| Primary Light | `#81D4FA` | Secondary elements |
| Accent | `#2962FF` | Hover states |
| Background | `#FAFAFA` | Slide background |
| Text | `#424242` | Body text |

Font: **Nunito** (400, 600, 700) — loaded automatically via Google Fonts.
