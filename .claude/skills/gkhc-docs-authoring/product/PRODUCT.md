# GitKraken Desktop: product notes for the docs-authoring skill

This folder is **local to this docs repo**. The shared skill files (SKILL.md,
references/, scripts/) are owned by GK-WP-HC-Design and replaced on every
distribution; `product/` never is. Edit it here.

| | |
| --- | --- |
| Content folder | `gitkraken-desktop/` (images in `_images/`) |
| WordPress category | `gitkraken-desktop`: pages publish at `/gitkraken-desktop/<slug>/` |
| Home page | `gitkraken-desktop-home` (`page_type: main-index`) |
| Nav file | `GK-WP-HC-Plugin/config/products/desktop.json` in GK-WP-HC-Design: label-only groups and links |
| Nav depth | up to 5 levels |
| Right-hand TOC | H2 and H3 |
| Unlabelled code panels | "Code" |

`config.json` beside this file holds the same facts in the form
`scripts/check_pages.py` and GK-WP-HC-Design's `preview/` read.

## Metadata (FRONTMATTER-SCHEMA.md)

Every page carries the Core fields (`references/metadata.md`).
Conditional fields required here: `os_support`, `git_hosts`, `integrations`, `hosted_variant`.
Allowed where they apply: `role_required`, `og_image`.
Constants: `product: GitKraken Desktop`.
`plan_required` values: `all`, `Community`, `Pro`, `Advanced`, `Business`, `Enterprise`, `insights-add-on`.

## Decisions for this help center

The settled design decisions are in GK-WP-HC-Design
`redesign-expansion/PER-PRODUCT-DECISIONS.md`, section "GitKraken Desktop". Record
conventions that only apply here (naming, recurring page shapes, words to use)
below this line.
