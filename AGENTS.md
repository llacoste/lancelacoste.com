# lancelacoste.com Repository Instructions

This repository contains the temporary personal website for `lancelacoste.com`.

## Scope

- Keep the site static: semantic HTML and CSS; add vanilla JavaScript only when required for meaningful behavior.
- Do not add dependencies, package managers, frameworks, build tools, or generated site output.
- Preserve a professional, restrained visual style appropriate for a platform and infrastructure engineering portfolio.
- Keep changes straightforward to replace when a fuller portfolio site is introduced.

## Visual Direction

- Maintain a dark, low-noise interface with subtle cool accents and clear hierarchy.
- Favor strong typography, generous spacing, and accessible contrast over decorative effects.
- Keep the layout responsive and keyboard-accessible on every content change.
- Use `icon.png` as the favicon/social-preview monogram asset; do not add it visibly to the page without direction.

## Content

- Primary identity and positioning copy live in `index.html`.
- The current email contact is `lance.lacoste@proton.me`.
- The LinkedIn URL is a placeholder until the canonical profile URL is confirmed.
- `icon.png` is the site icon and brandmark asset.

## Deployment

- GitHub Pages deploys the repository root through `.github/workflows/deploy.yml`.
- Preserve `CNAME` with `lancelacoste.com` as its only line unless the site's domain changes.
- Keep the public README concise; avoid provider-specific operations notes unless requested.

## Conventions

- Keep HTML semantic, CSS readable, and JavaScript limited to behavior that cannot be expressed in markup or styles.
- Avoid unrelated refactors; this site is intentionally small and disposable.
- Use Conventional Commits for repository history, such as `feat: add professional profile content`.
