---
name: wshy GitHub profile
description: A software publisher's catalogue with a cobalt masthead and native GitHub reading flow.
colors:
  publisher-cobalt: "#2850C8"
  night-wordmark: "#BDCEFF"
  night-band: "#2D4585"
  registration-mint: "#91D5C7"
  pale-stock: "#EAF0FF"
  navy-ink: "#203456"
  white-label: "#FFFFFF"
  night-stock: "#182238"
  night-heading: "#F0F5FF"
  night-label: "#D4E0FF"
typography:
  display:
    fontFamily: "Satoshi"
    fontWeight: 700
  headline-desktop:
    fontFamily: "PingFang SC, Microsoft YaHei, Noto Sans CJK SC, sans-serif"
    fontSize: "44px"
    fontWeight: 600
  headline-mobile:
    fontFamily: "PingFang SC, Microsoft YaHei, Noto Sans CJK SC, sans-serif"
    fontSize: "38px"
    fontWeight: 600
  label-desktop:
    fontFamily: "PingFang SC, Microsoft YaHei, Noto Sans CJK SC, sans-serif"
    fontSize: "27px"
    fontWeight: 400
  label-mobile:
    fontFamily: "PingFang SC, Microsoft YaHei, Noto Sans CJK SC, sans-serif"
    fontSize: "29px"
    fontWeight: 400
rounded:
  masthead: "20px"
components:
  masthead-desktop-light:
    backgroundColor: "{colors.pale-stock}"
    textColor: "{colors.navy-ink}"
    width: "100%"
  masthead-desktop-dark:
    backgroundColor: "{colors.night-stock}"
    textColor: "{colors.night-heading}"
    width: "100%"
  masthead-mobile-light:
    backgroundColor: "{colors.pale-stock}"
    textColor: "{colors.navy-ink}"
    width: "100%"
  masthead-mobile-dark:
    backgroundColor: "{colors.night-stock}"
    textColor: "{colors.night-heading}"
    width: "100%"
---

# Design System: wshy GitHub profile

## Overview

**Creative North Star: "The Software Publisher's Catalogue"**

A confident nameplate gives the author a recognizable identity; calm, open document space gives the projects room to explain themselves. Chinese copy, original English project names, and real product screenshots form an approachable technical catalogue.

This system owns the four SVG mastheads. GitHub owns the body typography, spacing, link states, heading rules, and disclosure controls. The surface strategy lives in [.impeccable/surface-briefs/profile.md](.impeccable/surface-briefs/profile.md).

**Key Characteristics:**
- Cobalt identity, pale stock, and one mint registration tile.
- Outlined wordmark with system-rendered Chinese lettering.
- Flat artwork and a single native reading column.
- Paired light/dark artwork and a separately composed mobile masthead.

## Colors

The palette resembles a publisher's blue ink on cool stock, with mint used only as a small registration accent. Frontmatter values are authoritative for the SVGs; screenshot and GitHub colors are independently owned.

- **Primary:** `publisher-cobalt` supplies the light wordmark and footer band. `night-wordmark` and `night-band` provide their dark-theme counterparts.
- **Secondary:** `registration-mint` supplies the decorative square in both themes.
- **Neutral:** `pale-stock` / `night-stock` are the masthead backgrounds; `navy-ink` / `night-heading` color the Chinese headline; `white-label` / `night-label` color the band label.

**The Paired Artwork Rule.** Change each semantic color role in both desktop and mobile assets, and review both themes together. The reviewed masthead text contrasts range from 5.99:1 to 14.50:1.

## Typography

The wshy wordmark is **Satoshi Bold converted to filled vector outlines**, not stroked text. No font binary or web-font loader ships. Its SVG transforms use scales of 0.194 on desktop and 0.164 on mobile; preserve the path geometry rather than replacing it with browser text.

Chinese artwork uses the CJK fallback stack and hierarchy in the frontmatter. Those sizes are SVG coordinate units and scale with the image: desktop headline on two lines, mobile headline on one. The label is slightly larger in the mobile artwork. Body text, H1/H2/H3, bold summaries, links, and small captions inherit GitHub's native styling; this repository defines no body font or type scale.

## Layout

Desktop SVGs use a (1200 × 300) viewBox; mobile SVGs use (600 × 380). The README's ordered `<picture>` sources choose mobile artwork at viewport widths of (600px) or less and use `prefers-color-scheme: dark` for dark variants. Keep the combined mobile/dark source first. All mastheads render at the available width with their aspect ratio preserved.

Within desktop artwork, the wordmark sits left, the headline right, and a full-width band begins at y=230. Mobile stacks the wordmark above the headline, with the band beginning at y=282. Coordinates belong to the artwork, not to a page spacing scale.

The document remains one fluid column. The Codex Token Monitor screenshot has a (640px) width attribute and shrinks with GitHub's image constraints; other project images use (100%) width. Inline contents and action links wrap naturally. Avoid fixed text columns.

## Elevation & Depth

The masthead is flat: solid fills, no gradients, shadows, or animation. Contrast and the footer band create separation. Product screenshots retain their own interface styling. The existing contribution animation remains behind a native `<details>` disclosure.

## Shapes

The masthead's outer rectangle uses the frontmatter radius in SVG coordinates; its rounded bottom corners continue through the footer band. The mint tile is a sharp square (44 × 44 desktop; 38 × 38 mobile). Do not apply the artwork's radius as an unscaled CSS radius to the README or screenshots.

## Components

- **Masthead:** four original SVG variants under `assets/profile-*.svg`; static, with an accessible title/description and a meaningful README image alternative. The sidecar previews these exact vectors.
- **Project entry:** native heading link, bold summary, paragraph, linked screenshot, contextual caption, and inline destinations. Preserve the same level of care for Codex Token Monitor and dsh-quota.
- **Contents and disclosure:** ordinary GitHub anchor links and native `<details>/<summary>`. Their hover, focus, and open states belong to GitHub; there are no custom buttons, cards, or inputs.
- **Evidence images:** existing public project screenshots, embedded directly. Keep historical/demo-data captions and provenance in [assets/SOURCES.md](assets/SOURCES.md). No new raster asset ships with this redesign.

## Do's and Don'ts

### Do:
- Do keep the profile understandable when images are unavailable.
- Do preserve wordmark outlines, CJK fallbacks, and all four theme/size variants.
- Do verify desktop/mobile and light/dark together after visual changes.
- Do keep project images linked to their repositories and document their provenance.

### Don't:
- Don't add gradients, an animated masthead, or a badge wall.
- Don't emulate a standalone website with fixed multi-column Markdown layouts.
- Don't convert native headings or links into decorative image text.
- Don't treat GitHub's body styling or embedded product UI as profile-owned tokens.
