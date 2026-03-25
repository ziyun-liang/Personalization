# Personalization prototypes

All personalization experiments live in a single **sidebar-driven hub** file: **[`personalization-features.html`](personalization-features.html)**.

Open it in a browser to see the left sidebar listing each prototype. Click an item to load it in the device frame on the right. Use **M** / **D** keys (or the toggle buttons) to switch between mobile and desktop views.

## Shared kit

The hub file references shared assets from the repo root:

- **Fonts:** `../_starter/NYTFonts/` (symlink to `Article-Overview/NYTFonts/`)
- **Logo:** `../Article-Overview/Assets/NYT-logo.svg`
- **Patterns:** see [`_starter/CLAUDE.md`](../_starter/CLAUDE.md) for conventions

## Current prototypes

| ID | Label | Description |
|----|-------|-------------|
| `inline-article-chat` | Inline Article Chat | Inline discussion panel anchored to the paragraph in view; article column with headline, deck, listen/util row, byline, Imperial body text, and a side chat panel with simulated comments per paragraph. |
| `clip-and-discuss` | Clip & Discuss | Full-flow social sharing prototype: tap a paragraph to clip it, preview a shareable card, pick a friend and send, then browse a "Shared with You" inbox with reply and read-full-story actions. |

## Adding a new prototype

1. Add a `<style>` block in `personalization-features.html` for the prototype's CSS.
2. Add a `<script>` IIFE that calls `window.__registerPrototype({ id, label, mount, unmount })`.
3. The sidebar auto-populates from the registry — no manual HTML edits needed.
4. Add a row to the table above.
