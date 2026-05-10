# Claude Theme for Obsidian

A warm, considered Obsidian theme inspired by Anthropic's Claude AI visual identity. Built around Claude's official brand palette — terracotta, pampas cream, and cloudy grey — it brings the same approachable, human quality to your daily note-taking that Claude brings to conversation.

## Preview

### Light Theme
<img width="1596" height="1196" alt="Screenshot 2026-05-10 at 21 02 50" src="https://github.com/user-attachments/assets/31e935fa-1fe3-4626-be7f-52bf870f5c80" />


### Dark Theme
<img width="1596" height="1196" alt="Screenshot 2026-05-10 at 21 03 52" src="https://github.com/user-attachments/assets/de3b25c4-bbdf-4837-99b7-f8b0a6fb6dd1" />


![Version](https://img.shields.io/badge/version-1.0-D97757?style=flat-square) ![Obsidian](https://img.shields.io/badge/Obsidian-1.0%2B-7A6AAA?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-4E8C5A?style=flat-square)

---

## Colour Palette

The theme is built on Claude's four official brand colours, with carefully derived shades for UI states.

| Name       | Hex       | Role                                             |
| ---------- | --------- | ------------------------------------------------ |
| Terracotta | `#D97757` | Primary accent — links, H1, interactive elements |
| Crail      | `#B85C38` | Hover states, deeper emphasis                    |
| Pampas     | `#F2F0EA` | Main canvas background                           |
| Cloudy     | `#B1ADA1` | Muted text, secondary UI                         |
| Ink        | `#2C2825` | Body text                                        |

Dark mode uses a matching family of warm near-blacks (`#1A1816` base) rather than the cold greys common in most themes.

---

## Features

**Full light and dark mode** — both sides of the theme use the same warm palette. Dark mode doesn't just invert; it uses a distinct family of warm brown-blacks that feel cohesive with the light mode.

**Heading hierarchy** — H1 renders in terracotta. H2 through H6 step down through warm ink to cloudy grey, giving your document structure an at-a-glance depth that plain black headings don't.

**Blockquotes** — a terracotta left border with a very subtle cream tint. Paragraph spacing inside blockquotes is tightened so multi-paragraph quotes read as a single unit, not a scattered list.

**Syntax highlighting** — varied, readable token colours across both edit and reading view:

- Keywords (`const`, `return`, `import`) — terracotta
- Strings — forest green
- Functions and class names — muted purple
- Numbers and booleans — amber
- Comments — warm grey italic
- Operators and punctuation — cloudy

Edit view (CodeMirror) and reading view (Prism) are targeted independently so both renderers display the same colours.

**Callouts** — six callout types with distinct, restrained colour treatments. Body text inside callouts is always normal ink weight, not the bold tinted text Obsidian defaults to.

| Callout                          | Colour          |
| -------------------------------- | --------------- |
| `note`, `info`                   | Terracotta      |
| `tip`, `hint`, `success`, `done` | Forest green    |
| `warning`, `caution`             | Amber           |
| `important`, `danger`, `bug`     | Deep terracotta |
| `question`, `faq`, `help`        | Muted purple    |

**Tags** — pill-shaped with a light terracotta tint and border. Clean and unobtrusive inline, easy to spot when scanning.

**Tables** — warm header background, subtle hover highlight, clean borders that don't compete with the content.

**Graph view** — terracotta for focused and tagged nodes, warm grey for the rest.

**Canvas** — selected nodes outlined in terracotta with a soft glow.

---

## Installation

### As a Theme (recommended)

1. Download `claude-theme.css`
2. Create the folder `<your-vault>/.obsidian/themes/Claude/`
3. Place the file inside and rename it to `theme.css`
4. Open Obsidian → **Settings → Appearance → Themes**
5. Select **Claude** from the dropdown

### As a Snippet

1. Place `claude-theme.css` in `<your-vault>/.obsidian/snippets/`
2. Open Obsidian → **Settings → Appearance → CSS Snippets**
3. Toggle the snippet on

---

## Fonts

The theme is designed around three typefaces. They are not bundled — install them locally first, then set them in Obsidian.

| Role        | Font           | Download                               |
| ----------- | -------------- | -------------------------------------- |
| Interface   | Inter          | https://rsms.me/inter/                 |
| Body / Text | Lora           | https://fonts.google.com/specimen/Lora |
| Monospace   | JetBrains Mono | https://www.jetbrains.com/lp/mono/     |

**To install on macOS:** unzip each download, select all `.ttf` / `.otf` files, right-click → Open With → Font Book → Install.

**To install on Windows:** unzip, select all font files, right-click → Install.

**To set in Obsidian:** Settings → Appearance → Font → type the font name exactly as listed above into the Interface, Text, and Monospace fields.

> The theme includes sensible system font fallbacks (`ui-serif`, `ui-sans-serif`, `ui-monospace`) so it degrades gracefully if the fonts aren't installed, but the serif body font (Lora) makes the biggest difference to the reading experience and is worth installing.

---

## Customisation

All colours are defined as CSS variables in the `:root` block at the top of the file. The three most impactful ones to change:

```css
:root {
  --claude-terracotta: #d97757; /* Primary accent colour */
  --claude-pampas: #f2f0ea; /* Canvas background */
  --claude-ink: #2c2825; /* Body text */
}
```

Change those three and the entire theme shifts character. The full palette is documented in the CSS with comments.

---

## Compatibility

- Obsidian 1.0 and later
- Live Preview (CodeMirror 6) ✓
- Reading View ✓
- Source Mode ✓
- Canvas ✓
- Graph View ✓
- Tested on macOS — should work on Windows and Linux

### Plugin compatibility

The theme does not override plugin-specific UI beyond basic colour variable inheritance. It has been lightly tested with:

- Dataview
- Calendar
- Tasks
- Templater

If you find a plugin whose UI clashes, open an issue and include a screenshot.

---

## File Structure

```
Claude/
├── theme.css               — main theme file
├── claude-theme-preview.md — full markdown element showcase
└── README.md               — this file
```

---

## Changelog

### v2.0

- Refined terracotta from `#DE7356` to `#D97757` — richer, closer to the actual Claude UI
- Fixed callout body text rendering as bold and tinted
- Fixed blockquote paragraph spacing creating large gaps between paragraphs
- Added dedicated Prism token rules for reading view syntax highlighting — edit and preview now match
- Introduced varied syntax palette: green strings, purple functions, amber numbers
- Bold text changed from terracotta to warm ink — less distracting in long-form reading
- Added `==highlight==` support via explicit `mark` rule
- Sidebar background distinguished from canvas background
- Dark mode surfaces deepened and warmed

### v1.0

- Initial release

---

## License

MIT — use it, modify it, share it. Attribution appreciated but not required.

---

_Designed to make the place where you think feel as considered as the tools you think with._
