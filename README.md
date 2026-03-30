# Notion Motion — Obsidian Theme

A pixel-accurate recreation of [Notion](https://notion.so)'s UI for [Obsidian](https://obsidian.md).
Supports **Light mode** and **Dark mode** out of the box.

---

## Preview

| Light Mode | Dark Mode |
|-----------|-----------|
| White background (`#ffffff`), warm gray text (`#37352f`) | Dark background (`#191919`), soft white text |
| Notion's classic clean sidebar | Same layout, dark surface (`#202020`) |

---

## Features

- **Pixel-accurate Notion colors** — every surface, text shade, and border matches Notion's design system
- **Light & Dark mode** — automatic, follows your system preference or Obsidian's setting
- **Inter font** — loaded via Google Fonts, matches Notion's typeface exactly
- **JetBrains Mono** for code blocks
- **Full component coverage**: headings, lists, checkboxes, tables, callouts, code blocks, blockquotes, tags, embeds, graph view, settings, modals, context menus, sidebar, status bar, ribbon

---

## Color Palette

### Light Mode

| Token | Value | Usage |
|-------|-------|-------|
| Background | `#ffffff` | Main editor |
| Surface | `#f7f6f3` | Sidebar, secondary panels |
| Text primary | `#37352f` | Body copy |
| Text muted | `rgba(55,53,47,0.65)` | Labels, captions |
| Text faint | `rgba(55,53,47,0.40)` | Placeholders, hints |
| Accent (blue) | `#2383e2` | Links, interactive elements |
| Border | `#e9e9e7` | All dividers and outlines |
| Code background | `rgba(135,131,120,0.15)` | Inline & block code |
| Highlight | `rgba(251,243,219,1)` | `==highlighted==` text |

### Dark Mode

| Token | Value | Usage |
|-------|-------|-------|
| Background | `#191919` | Main editor |
| Surface | `#202020` | Sidebar, secondary panels |
| Text primary | `rgba(255,255,255,0.81)` | Body copy |
| Text muted | `rgba(255,255,255,0.443)` | Labels, captions |
| Text faint | `rgba(255,255,255,0.28)` | Placeholders, hints |
| Accent (blue) | `#529cca` | Links, interactive elements |
| Border | `#373737` | All dividers and outlines |
| Code background | `rgba(135,131,120,0.15)` | Inline & block code |
| Highlight | `rgba(120,100,40,0.5)` | `==highlighted==` text |

---

## Typography

| Context | Font | Size | Weight |
|---------|------|------|--------|
| Body text | Inter | 16px | 400 |
| H1 (page title) | Inter | 2.5em | 700 |
| H2 | Inter | 1.875em | 600 |
| H3 | Inter | 1.5em | 600 |
| H4 | Inter | 1.25em | 600 |
| H5/H6 | Inter | 0.875em | 600, uppercase |
| Code | JetBrains Mono | 0.875em | 400 |
| UI / Sidebar | Inter | 13–14px | 400–500 |

---

## Installation

### Option A — Community Themes (recommended)

1. Open Obsidian → **Settings** → **Appearance**
2. Click **Manage** next to Themes
3. Search for **Notion Motion**
4. Click **Install and use**

### Option B — Manual install

1. Download the [latest release](../../releases/latest) (`notion-motion-vX.X.X.zip`)
2. Unzip and copy `theme.css` + `manifest.json` into:
   ```
   <your-vault>/.obsidian/themes/Notion Motion/
   ```
3. Open Obsidian → **Settings** → **Appearance** → **Themes** → select **Notion Motion**

### Option C — Install from source

```bash
cd /path/to/your/vault/.obsidian/themes/
git clone https://github.com/<your-username>/obsidian-motion-theme "Notion Motion"
```

---

## Callout Styles

The theme styles all standard Obsidian callout types:

```markdown
> [!info] Info
> Blue — informational notes

> [!warning] Warning
> Yellow — caution

> [!error] Error
> Red — errors and danger

> [!success] Success
> Green — done, check, success

> [!tip] Tip
> Green — hints and tips

> [!question] Question
> Yellow — FAQ and questions
```

---

## Supported Elements

| Element | Styled |
|---------|--------|
| Headings H1–H6 | ✅ |
| Paragraphs & body | ✅ |
| Bold, italic, strikethrough | ✅ |
| `==Highlight==` | ✅ |
| Inline code | ✅ |
| Code blocks (with language label) | ✅ |
| Syntax highlighting | ✅ |
| Blockquotes | ✅ |
| Callouts (all types) | ✅ |
| Unordered lists | ✅ |
| Ordered lists | ✅ |
| Task lists / checkboxes | ✅ |
| Tables | ✅ |
| Horizontal rules | ✅ |
| Tags | ✅ |
| Internal & external links | ✅ |
| Images | ✅ |
| Footnotes | ✅ |
| Embeds | ✅ |
| Frontmatter / Properties panel | ✅ |
| File explorer / sidebar | ✅ |
| Tabs | ✅ |
| Ribbon | ✅ |
| Status bar | ✅ |
| Quick switcher / command palette | ✅ |
| Context menu | ✅ |
| Settings panel | ✅ |
| Toggle switches | ✅ |
| Graph view | ✅ |
| Scrollbars | ✅ |

---

## Releasing a New Version

Releases are automated via GitHub Actions. To publish a new release:

```bash
# Bump version in manifest.json first (optional — CI updates it automatically)
git tag v1.2.0
git push origin v1.2.0
```

The pipeline will:
1. Read the version from the tag
2. Update `manifest.json` with the new version
3. Package `theme.css` + `manifest.json` into a zip
4. Generate a changelog from commit messages
5. Create a GitHub Release with all artifacts attached

Pre-release versions (e.g. `v1.2.0-beta.1`) are automatically marked as pre-releases.

---

## Development

The entire theme lives in a single file: [`theme.css`](./theme.css).
It is structured in numbered sections for easy navigation:

| Section | Content |
|---------|---------|
| 0 | Google Fonts import |
| 1–2 | Light / Dark mode CSS variables |
| 3 | Base typography |
| 4–5 | App layout, sidebar |
| 6 | Editor |
| 7–14 | Content: headings, text, links, code, blockquotes, lists, tables |
| 15–17 | HR, tags, callouts |
| 18–20 | Inline formatting, frontmatter |
| 21–25 | Search/modal, ribbon, status bar, buttons, inputs, scrollbars |
| 26–35 | Embeds, graph, file explorer, properties, tooltips, context menu |
| 36–42 | Settings, toggles, active line, print, reduced motion |

To contribute, fork the repo and open a PR against `main`.

---

## License

[MIT](./LICENSE)
