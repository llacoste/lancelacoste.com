# lancelacoste.com Repository Instructions

Personal website for `lancelacoste.com` — a **public** repo.

## Scope

- The site is built with **Astro** (v5): pages in `src/pages`, a shared `Base.astro` layout, content collections for `blog` and `projects` (Markdown/MDX, configured in `src/content.config.ts`), styles in `src/styles/global.css`. Build with `npm run build`.
- Keep dependencies and footprint minimal; don't add heavy UI frameworks or libraries without a clear reason.
- Preserve a professional, restrained visual style appropriate for a platform and infrastructure engineering portfolio.

## Visual Direction

- Maintain a dark, low-noise interface with subtle cool accents and clear hierarchy.
- Favor strong typography, generous spacing, and accessible contrast over decorative effects.
- Keep the layout responsive and keyboard-accessible on every content change.
- Use `icon.png` as the favicon/social-preview monogram asset; do not add it visibly to the page without direction.

## Content

- Primary identity and positioning copy live in `src/pages/index.astro`; nav lives in `src/layouts/Base.astro`.
- `blog/` and `projects/` are content collections — they render a coming-soon state while empty.
- `/resume` (`src/pages/resume.astro`) embeds the résumé PDF served from the public mirror at `https://resume.lancelacoste.com/resume.pdf`. Don't commit a PDF here; it's owned by the résumé pipeline.
- The current email contact is `lance.lacoste@proton.me`.

## IP guardrail

This site is **public**. Do not reference employer-internal system codenames or
confidential business/financial figures anywhere in content (projects, blog,
résumé copy). The embedded résumé is generalized at its source (the private
résumé repo); keep all public copy at that same generalized level. When in
doubt, describe systems by function, not by internal name.

## Deployment

- `.github/workflows/deploy.yml` builds the Astro site and deploys to GitHub Pages on push to `main`; PRs run a build check.
- Preserve `public/CNAME` with `lancelacoste.com` as its only line unless the site's domain changes.
- Keep the public README concise; avoid provider-specific operations notes unless requested.

## Conventions

- Use Conventional Commits (e.g. `feat: add projects index`).
- Every change goes through a branch + PR, squash-merged to `main`.
- Avoid unrelated refactors; keep changes focused.
