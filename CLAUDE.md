# CLAUDE.md

Guidance for AI agents working in this repository.

## What this is

A static marketing website for **The Flapjack Bros**, a bakery/shop that
formed in 2026. Source content lives in `project-description.md` — treat
it as the source of truth for copy and facts about the business:

- Heading: The Flapjack Bros
- About Us: formed in 2026
- Where to find us: near the English Channel at 2 St Hilda's Road, Hythe.
  Visitors get a 20% discount and a free poster. Cash only.
- What we sell: flapjacks, chocolate-popcorn biscuits, and other treats.

If `project-description.md` is updated, the site content in
`site/flapjack-brothers/index.html` should be updated to match.

## Structure

- `project-description.md` — plain-text description of the business used
  as the content source for the site.
- `site/flapjack-brothers/index.html` — the live single-page site. Plain
  HTML/CSS (Fredoka + Nunito via Google Fonts), no build step, no
  framework, no JS dependencies.
- `site/shadoll/index.html` — an unrelated sample/reference site
  (a software studio landing page). Do not confuse it with the
  Flapjack Bros site or copy its branding/content into it.

## Conventions

- Keep the site a single self-contained HTML file (inline `<style>`,
  no build tooling) unless the user asks for a framework/build step.
- Preserve the warm bakery color palette (cream/oat/caramel/chocolate)
  and rounded, playful styling already established in
  `site/flapjack-brothers/index.html`.
- Facts about the shop (address, discount, payment method, products)
  must stay consistent with `project-description.md`.

## Running the site

It's a static file with no server-side logic. Serve it locally, e.g.:

```
cd site/flapjack-brothers
python3 -m http.server 8765
```

Then open `http://localhost:8765/`.
