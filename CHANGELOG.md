# Changelog

## 1.1.19 — 2026-07-22

- Fixed Typora's active paragraph becoming faint while editing by keeping the `.md-expand` container out of the auxiliary Markdown text color rule.
- Limited fenced-code active-line backgrounds to the editor that actually has focus, so Typora and Obsidian no longer leave the first or previously edited code line looking different after the cursor moves away.

## 1.1.18 — 2026-07-17

- Restored Obsidian Reading View quote cards to the same spacing, radius, and nesting rhythm used by the Typora themes.
- Removed the extra Obsidian-only compact override that caused quoted fenced code blocks to gain excessive whitespace and visual seams.
- Kept the outer quote shadow while allowing nested quotes to use a quieter surface without repeated shadows.

## 1.1.17 — 2026-07-17

- Refined Obsidian quote cards, nested quotes, quoted lists, tasks, and code blocks in Reading View and Live Preview.
- Tightened list spacing, improved light code contrast, and expanded the manual regression fixtures.
- Fixed long inline code wrapping and removed unwanted seams around nested quote content.
- Made Reading View tables fill their outer frame instead of leaving a blank area on the right.
- Balanced long external-link wrapping so a few characters and the external-link icon are not stranded on the last line.

## 1.1.16 — 2026-07-16

- Fixed Obsidian Live Preview tables whose nested cell editors inherited the document's vertical page padding and created oversized rows.

## 1.1.15 — 2026-07-16

- Fixed unreadable ribbon and icon-control tooltips by explicitly pairing their text color with the theme surface.
- Improved light-mode interaction contrast for links, wiki links, backlinks, badges, and blue buttons.

## 1.1.14 — 2026-07-16

- Synced Typora fenced code blocks with the Apple-inspired light and dark treatment used in Obsidian.
- Added separate Paper and Midnight code palettes, toolbar bands, traffic-light controls, active-line feedback, and high-contrast cursors.
- Replaced Typora Paper and Midnight preview images with real screenshots of the updated code blocks.

## 1.1.13 — 2026-07-16

- Fixed system notices and plugin-update progress messages whose text could become unreadable on light surfaces.
- Added explicit light and dark notice colors, borders, close-button treatment, and Esther blue progress feedback.

## 1.1.12 — 2026-07-15

- Redesigned Obsidian fenced code blocks with separate Apple-inspired light and dark palettes in Reading View and Live Preview.
- Increased code-editor cursor contrast and added a subtle active-line highlight.
- Added a Style Settings option that reveals file explorer action buttons on hover while preserving the existing default behavior.
- Refined the file explorer hierarchy with restrained editorial folder styling and cleaner active-file treatment.
- Removed file explorer indentation guides for an uncluttered sidebar in both color modes.

## 1.1.11 — 2026-07-15

- Fixed repeated dropdown arrows in Obsidian settings on dark mode and some Windows configurations.
- Preserved Obsidian's native dropdown icon while applying the Esther surface color.
- Improved the contrast of the active file title in the dark file explorer.

## 1.1.10 — 2026-07-15

- Added a concise English overview and community-directory installation guide.
- Documented Style Settings customization options.
- Replaced the abbreviated license notice with the canonical CC BY-NC-SA 4.0 legal text.
- Removed all `!important` declarations from the Obsidian theme.
- Replaced partially supported masks and underline properties with compatible CSS.
- Kept the quotation-card appearance while reducing compatibility warnings.

## 1.1.9 — 2026-07-15

- Prepared the first public GitHub release.
- Added adaptive Obsidian light and dark modes.
- Added Typora Paper and Midnight themes.
- Unified Obsidian quote backgrounds in Reading View and Live Preview.
- Positioned quote marks beside the body text without clipping.
- Styled wiki links, embeds, backlinks and outgoing links.
- Changed text highlights to a lower-half marker stroke.
- Added store-ready screenshots, attribution and submission notes.
