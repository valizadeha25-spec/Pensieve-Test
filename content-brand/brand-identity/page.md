# Brand Identity

PamAI’s brand identity is calm, editorial, and confident—closer to a well-set magazine than a SaaS ad, with lots of whitespace.^\[1\]^ (`data:18`) Its palette is soft, earthy, and warm, using off-whites and warm grays with a single muted-olive accent.^\[2\]^ (`data:18`) `Brand_Assets/` at the repository root is the source of truth; `core/brand.md` is the working reference and should be updated alongside asset changes.^\[3\]^ (`data:18`)

## Typography

Pam uses two typefaces, no others.^\[4\]^ (`data:18`) Plein in Regular, Medium, and Bold is the display face for headlines, hero text, hook slides, and high-impact numbers.^\[5\]^ (`data:18`) Switzer in Light, Regular, Medium, and Semibold is the body face for paragraphs, labels, captions, UI, and supporting copy.^\[6\]^ (`data:18`) The WOFF2 font files live in `Brand_Assets/Fonts/` and are mirrored into `.claude/skills/linkedin-visuals/brand/fonts/`.^\[7\]^ (`data:18`)

The base type scale runs from `xs` 12 through `5xl` 48 px: `xs` 12, `sm` 14, `base` 16, `lg` 18, `xl` 20, `2xl` 24, `3xl` 30, `4xl` 36, and `5xl` 48.^\[8\]^ (`data:18`) For 1080×1350 carousels, the scale is amplified according to the skill’s `brand/tokens.css`.^\[9\]^ (`data:18`)

## Color system

The olive is an accent rather than a flood, and the palette avoids high saturation.^\[10\]^ (`data:18`)

- Backgrounds: `#fafaf8` background, `#f2f0eb` surface, `#e8e5de` surface-2, `#ece8e1` panel, and `#26211c` ink panel.^\[11\]^ (`data:18`)
- Text: `#1a1814` primary, `#6b6960` secondary, `#9a9890` muted, and `#c4c1b8` disabled.^\[12\]^ (`data:18`)
- Green accent: `#7f8d6a` primary, `#6f7b5d` dark, `#b8c2ab` light, and `#eef1e8` subtle.^\[13\]^ (`data:18`)
- Borders: `#e2ded6` default and `#d0ccc4` strong.^\[14\]^ (`data:18`)

The reference separately records product-UI status colors: idea `#fae8b4`, in-progress `#f5d5b0`, review `#d8c4e0`, on-track `#c4e8d8`, at-risk `#f8d4b8`, blocked `#f2c4c8`, and milestone `#d4c8e8`.^\[15\]^ (`data:18`)

## Shape language and marks

Radii are `sm` 6, `md` 10, `lg` 16, `xl` 24, `4xl` 32, and `full` 9999 px; the system calls for generous, soft corners, with pills and circles for tags and avatars.^\[16\]^ (`data:18`)

The Pam logo is `Brand_Assets/Pam-Logo.jpg`, a green concentric-wave “P” mark on white. Use the green mark on light backgrounds and reverse it to off-white on the ink panel `#26211c`.^\[17\]^ (`data:18`) Give the logo air: never crowd it, recolor it outside the palette, or place it on a busy background.^\[18\]^ (`data:18`)

## Author identities

Content bylines are per-post: each post is stamped with its author’s identity, not always the company.^\[19\]^ (`data:18`)

- Amir uses `Brand_Assets/Amir-Profile.png`, a headshot shot on brand olive, with the line “Amir Valizadeh · Helping people manage their projects at @PamAI”.^\[20\]^ (`data:18`)
- Niyayesh is marked as needing a headshot, handle, and headline.^\[21\]^ (`data:18`)
- Pam uses `Brand_Assets/Pam-Logo.jpg` as the company-brand author identity.^\[22\]^ (`data:18`)

## Editorial principles

Each slide should carry one idea; the design serves the sentence rather than the other way around.^\[23\]^ (`data:18`) Olive should mark emphasis—one number, one underline, or one rule—not become the background.^\[24\]^ (`data:18`) Type does the work: Plein carries impact, Switzer carries clarity, and decoration should not duplicate what the typography can already deliver.^\[25\]^ (`data:18`)

## Implementation boundary

The working reference flags a separate dashboard migration: it records `dashboard/app/globals.css` as using DM Sans and Playfair Display, which predates the brand, and specifies Switzer and Plein as the correct fonts.^\[26\]^ (`data:18`)

## Sources
- [core/brand.md](https://github.com/valizadeha25-spec/Pam-CompanyBrain/blob/main/core/brand.md) (`data:18`)
