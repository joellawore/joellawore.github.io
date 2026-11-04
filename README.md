# Joel Lawore — Portfolio

Lightweight static portfolio for GitHub Pages. No build step or framework is required.

## Local preview

From the repository root, run:

```powershell
python -m http.server 4173 --bind 127.0.0.1
```

Open <http://127.0.0.1:4173/>. The redesign is intended for review on its dedicated branch; it has not been published.

Files:
- [Home](./index.html) — introduction, portrait, and a personal passage about music
- [Work](./work.html) — Wabtec, teaching, and three selected projects, with optional depth
- [Notes](./notes.html) — short writing; the first note is a draft for review
- [Project studies](./projects/) — engineering decisions, diagrams, results, and limitations
- [Styles](./styles.css) — shared typography, colors, and responsive layouts
- [Résumé](./assets/joel-lawore-resume.pdf) — direct PDF link
- [Design brief](./DESIGN_BRIEF.md) — current direction and constraints
- [Current review](./docs/personal-home-review.md) — validation and performance for the personal-home revision
- [Earlier review](./docs/redesign-review.md) — historical validation for the first redesign

The site uses system fonts, responsive WebP portrait images, and no JavaScript. It has no runtime dependencies or build step. Project diagrams are HTML and remain readable without image loading. Native disclosures provide optional detail. Navigation is Home / Work / Notes; Email and the direct résumé PDF are in the shared footer. The old About URL forwards to the experience section on Work.

## Links already configured

- GitHub: https://github.com/joellawore
- LinkedIn: https://www.linkedin.com/in/joellawore
- Email: joellawore@gmail.com

## Academic-integrity note

The public site intentionally does **not** link to or reproduce source code for course projects. Even where old Git remotes may exist, the portfolio treats CS 15, CS 40, CS 105, and other course work as private unless explicitly cleared for publication.

## Content and assets

Project claims come from the previous portfolio and the current résumé. Benchmark results retain their evaluation context; no public coursework repositories or invented demo links are added.

The home portrait uses optimized 320 × 400 and 640 × 800 derivatives of the supplied sweater headshot. Original portrait files and the current résumé are preserved. The portrait has explicit dimensions and responsive source selection. There are no separate below-the-fold image assets; add `loading="lazy"` and dimensions if future project images are introduced. The drawing-room reference images are mood references, not site assets.

The first note retells only the listening account supplied by Joel. It is marked as a draft, is excluded from indexing, and contains no added music-history claims or invented personal experiences. The site and note remain unpublished pending review.
