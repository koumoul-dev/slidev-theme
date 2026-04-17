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

### `<Kpi />`

A compact KPI card showing a value, a label, and an icon passed as a child tag. Use any MDI icon (bundled with this theme) or any other Iconify collection you install.

| Prop    | Type                                 | Description                                        |
|---------|--------------------------------------|----------------------------------------------------|
| label   | `string`                             | Text shown under the value                         |
| value   | `string \| number`                   | The metric to display                              |
| variant | `'flat' \| 'card' \| 'card-primary'` | Visual style — defaults to `flat` (no background). `card` uses a white card with shadow, `card-primary` uses a primary-colored card with white text. |

```markdown
<Kpi label="Active Users" value="12.4k">
  <mdi-account-group />
</Kpi>
```

Arrange multiple KPIs with a grid:

```markdown
<div class="grid grid-cols-3 gap-6">
  <Kpi label="Datasets" value="847"><mdi-database /></Kpi>
  <Kpi label="Uptime" value="99.9%"><mdi-chart-line /></Kpi>
  <Kpi label="Regions" value="12"><mdi-earth /></Kpi>
</div>
```

## Icons

Material Design Icons are bundled with this theme — use them directly in any slide:

```markdown
<mdi-rocket-launch />
<mdi-account-circle class="text-3xl" />
```

Browse available icons at [icones.js.org/collection/mdi](https://icones.js.org/collection/mdi). Other Iconify collections work too — just `npm i @iconify-json/<collection>` in your own project.

## Brand Colors

| Color | Hex | Usage |
|-------|-----|-------|
| Primary | `#1976D2` | Headings, links, accents |
| Primary Light | `#81D4FA` | Secondary elements |
| Accent | `#2962FF` | Hover states |
| Background | `#FAFAFA` | Slide background |
| Text | `#424242` | Body text |

Font: **Nunito** (400, 600, 700) — loaded automatically via Google Fonts.
