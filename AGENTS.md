# AGENTS.md

## Project

This repository is the `IBCCS TAX Uzbekistan` landing page.  
Single file: `index.html` — all styles, markup, and JS are inline in this one file.  
Do not create separate CSS or JS files unless explicitly asked.

The page is for the Uzbekistan office only. Do not position it as a Georgia page or global corporate page, except where brief group context is helpful.

---

## Brand Naming

- Always use `IBCCS TAX Uzbekistan` as the company name in page content.
- Do not use `IPCCS`, `IBCCS TAX Georgia`, or other variants unless quoting source material.
- Group context: refer to `IBCCS TAX Group`.

---

## Team (current confirmed roles)

| Name | Role |
|---|---|
| Ketevan Aghoshashvili | Founder |
| Irakli Arjevanidze | Director |
| Farrukh Kholmatov | Account Manager |

Use only confirmed names and roles. Do not invent titles.

---

## Languages

- `index.html` is English by default.
- Language toggle (EN / RU / 中文) is present in the header and mobile menu.
- Russian and Chinese content has **not** been written yet. Do not generate translations unless explicitly asked.
- When translations are added, use `data-lang` attributes on text nodes and switch via JS — do not duplicate the full HTML.

---

## Design System

### Colors
| Token | Value | Use |
|---|---|---|
| `--g` | `#5EA397` | Brand green — accents, CTAs, active states, italic headings |
| `--navy` | `#0C1220` | Page background |
| `--navy2` | `#111929` | Section backgrounds (solid dark sections) |
| `--text` | `#FFFFFF` | Primary text |
| `--muted` | `rgba(255,255,255,0.90)` | Body paragraphs |
| `--muted2` | `rgba(255,255,255,0.78)` | Labels, secondary text, footer |
| `--border` | `rgba(255,255,255,0.07)` | Subtle dividers |
| `--border-strong` | `rgba(255,255,255,0.13)` | Visible borders |

### Typography
- **Headings:** `Cormorant Garamond` serif, `font-weight: 600`
- **Heading italic/green `<em>`:** always `font-weight: 400` (thin cursive — do not make bold)
- **Body / UI:** `Barlow` sans-serif, `font-weight: 400` (never 300)
- **Labels / nav / buttons:** `Barlow Condensed`, `font-weight: 600`, uppercase, wide letter-spacing
- **Base font size:** `17px` for paragraphs; `18px` for hero sub

### Section Backgrounds
Alternate solid dark and photo-overlay sections:

| Section | Background |
|---|---|
| Hero | `tashkent1.jpg` (with dark gradient overlay) |
| About | `--navy2` solid |
| Services | `--navy` solid |
| Statement | `tashkent3.jpg` photo overlay |
| Sectors | `tashkent4.jpg` photo overlay |
| Team | `--navy2` solid |
| Contact | `tashkent6.jpg` photo overlay |

Photo overlay opacity is ~72–80% dark (`rgba(12,18,32,0.72–0.80)`).  
On mobile, set `background-attachment: scroll` (not `fixed`) for photo sections.

### Logo
- File: `assets/ibccs logo.png`
- **Do not apply** `filter: brightness(0) invert(1)` — the logo has its own brand colors (half green).
- Header: `height: 28px`, no filter.
- Footer: `height: 24px`, no filter.

### Spacing rhythm
- Section padding: `96–112px 0`
- Wrap max-width: `1240px`, padding `0 52px` (desktop), `0 28px` (tablet), `0 20px` (mobile)
- Grid gaps: `80–96px` (two-column layouts), `24px` (team cards)

---

## Components

### Hero
- `min-height: 100vh` — must fill the full viewport.
- Headline: Cormorant Garamond, `clamp(48px, 6vw, 84px)`, weight 600.
- Italic word ("Opportunities"): weight 400, color `--g`.
- Aside panel (service list) hidden on mobile.

### Navigation
- Desktop: fixed header, `height: 68px`, blur backdrop.
- Mobile (≤640px): desktop nav is hidden; hamburger button shown top-right.
- Hamburger opens a full-screen dark overlay with large serif nav links + language toggle.
- Language buttons use `data-lang="en|ru|zh"` and `.active` class (green).
- Both desktop and mobile lang toggles must stay in sync (toggle all `.lang-btn[data-lang=x]` at once).

### Headings with green italic
All `<em>` inside headings follow the same rule: `font-style: italic; font-weight: 400; color: var(--g)`.  
Never override this to bold.

### Team cards
- 3-column grid, `gap: 24px`.
- Photo aspect ratio: `3 / 4.2` (portrait).
- Member info: name in Cormorant Garamond weight 600, role in Barlow weight 400.

---

## Content Rules

- Write for Uzbekistan and Tashkent specifically.
- Do not invent case studies, statistics, awards, certifications, client logos, or legal claims.
- Keep copy factual and adaptable for later review.
- Placeholder contact details (address, email, phone, social URLs) are acceptable until confirmed.

### Key phrases to preserve
- `Turn Challenges into Opportunities`
- `Your Gateway to Growth`
- `highest level of expertise, security, and confidentiality`
- `Every client is unique`

---

## Services (confirmed pillars)

1. Market Entry
2. Finance & Taxation
3. Business Registration
4. Legal Services
5. Expat Services
6. Startup Services

Do not add or remove services without explicit client confirmation.

---

## Source of Truth

If sources conflict, prefer the latest direct user instruction.

- `assets/Content Details .docx` — approved copy
- User-provided instructions in conversation

---

## Working Style

- Edit `index.html` directly. Do not create new HTML files or versioned copies.
- Make targeted edits — do not rewrite sections that weren't asked about.
- Do not add comments, docstrings, or explanatory code annotations.
- Do not introduce new dependencies (no frameworks, no CDN libraries beyond the existing Google Fonts).
- Keep the architecture ready for Russian/Chinese language content to be wired in later via JS.
