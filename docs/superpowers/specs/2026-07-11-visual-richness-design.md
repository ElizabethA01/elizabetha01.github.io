# Portfolio Visual Richness — Design

## Purpose

This site exists primarily to support Elizabeth's applications for tech awards (e.g. Tech Women 100) and speaking engagements, both of which typically request a personal website alongside LinkedIn. It also serves recruiters/hiring managers and prospective mentees. Because award panels and event organizers skim quickly, the site needs to read as **credible and polished**, not as a design-flair showcase.

## Direction

Refine the existing visual identity rather than replace it — Fraunces (serif display) + Inter (body) + IBM Plex Mono (labels), warm off-white/near-black with a copper accent (`#A6763E`), "monochrome, on purpose" ethos. Three genuinely different directions (Blueprint/navy-technical, Terminal/dark-monospace, Editorial Warm/terracotta-serif) were mocked up and rejected in favor of staying with the current identity.

Intensity level: **"Noticeably rich"** — confident but professional. A louder "maximalist" treatment (giant bleeding background numerals, cards that fully invert to black on hover, heavier motion) was also prototyped for comparison and explicitly not chosen, since it reads as more "design portfolio" than "credible engineer's site."

## Changes (validated via `index-preview.html` prototype)

**Depth**
- Case-study cards: individual rounded cards (not a seamless divided block) with a resting border, lifting to a soft shadow + background swap on hover
- Stat/breaker section: subtle radial copper glow layered behind the existing grid texture
- Header: backdrop blur + soft shadow once scrolled past the hero, replacing the flat sticky bar
- New circular photo-placeholder frame in the hero (gradient fill, border, shadow) — ready for a real photo later without further redesign

**Motion**
- Sections fade + slide up once on scroll into view (`IntersectionObserver`, non-repeating)
- Existing stat counter animation (89,085 → 393) kept as-is
- Case-study cards lift on hover; nav links and card links get animated underline/shift on hover
- Speaking/community rows get a background + indent shift on hover
- All motion respects `prefers-reduced-motion`

**Typography & spacing rhythm**
- Slightly increased section padding (80px → 88px) for more breathing room
- Case-study card line-height and spacing loosened
- Existing mono-label system (`01 — ABOUT` etc.) kept as the section rhythm marker, unchanged

## Out of scope

- Real photo (placeholder frame only)
- Copy/content pass (explicitly flagged as "still to come" in the existing footer note)
- Maximalist treatment (prototyped, rejected)

## Implementation note

The validated prototype already exists at `index-preview.html` in the repo root. Implementation is promoting that file to replace `index.html`, then removing the prototype files (`index-preview.html`, `index-preview-maximalist.html`) and the `.superpowers/` brainstorm session directory.
