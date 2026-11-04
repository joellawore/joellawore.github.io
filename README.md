# Joel Lawore — Portfolio

Lightweight static portfolio for GitHub Pages. No build step or framework is required.

## Local preview

From the repository root, run:

```powershell
python -m http.server 4173 --bind 127.0.0.1
```

Open <http://127.0.0.1:4173/>. The redesign is intended for review on its dedicated branch; it has not been published.

Files:
- [Home](./index.html) — introduction, availability, portrait, and contact links
- [Work](./work.html) — three selected projects and two additional studies
- [About](./about.html) — Tufts, Wabtec, teaching, and personal background
- [Project studies](./projects/) — engineering decisions, diagrams, results, and limitations
- [Styles](./styles.css) — shared typography, colors, and responsive layouts
- [Résumé](./assets/joel-lawore-resume.pdf) — direct PDF link
- [Review report](./docs/redesign-review.md) — validation and before/after performance

The site uses system fonts, responsive WebP portrait images, and no JavaScript. It has no runtime dependencies or build step. Project diagrams are HTML and remain readable without image loading.

## Links already configured

- GitHub: https://github.com/joellawore
- LinkedIn: https://www.linkedin.com/in/joellawore
- Email: joellawore@gmail.com

## Academic-integrity note

The public site intentionally does **not** link to or reproduce source code for course projects. Even where old Git remotes may exist, the portfolio treats CS 15, CS 40, CS 105, and other course work as private unless explicitly cleared for publication.

## Content and assets

Project claims come from the previous portfolio and the current résumé. Benchmark results retain their evaluation context; no public coursework repositories or invented demo links are added.

The home portrait uses optimized 320 × 400 and 640 × 800 derivatives of the existing sweater headshot. Original portrait files and the pre-existing résumé modification are preserved. The portrait is above the fold, with explicit dimensions and responsive source selection. There are no below-the-fold image assets; add `loading="lazy"` and dimensions if future project images are introduced.
