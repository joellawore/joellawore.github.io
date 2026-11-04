# Personal-home revision review

November 4, 2026. [Local preview](http://127.0.0.1:4173/) · [First-note draft](http://127.0.0.1:4173/notes/i-want-to-be-adored.html) · [Current brief](../DESIGN_BRIEF.md).

## Direction and content

The [brief](../DESIGN_BRIEF.md) was updated before the implementation. The site now uses parchment, deep brown, and burgundy, with a narrower reading measure, modest Georgia headings, and system sans-serif text. The drawing-room references informed the palette and spacing; no room imagery or decorative textures were added.

- [Home](../index.html) introduces Joel plainly, mentions music, philosophy, and campus ministry naturally, and includes a short listening passage with a link to Notes. The supplied portrait is smaller and responsive.
- [Work](../work.html) combines Wabtec experience, Tufts teaching, and three selected projects. Native disclosures provide optional detail. The older two studies are available through one disclosure. There is one understated availability mention, on this page.
- [Notes](../notes.html) contains one actual [draft](../notes/i-want-to-be-adored.html), based only on Joel’s account of hearing “I Want to Be Adored” on a bus to New Jersey. No lyrics, dates, music history, or additional personal experiences were added. The draft is marked for review and has a `noindex` directive.
- Project explanations, benchmark context, limitations, and private-coursework notices remain intact. The uScheme timing is now confined to its project page rather than repeated in the overview.
- Primary navigation is Home / Work / Notes. Email and the direct résumé PDF are quiet footer links on every content page. The former [About URL](../about.html) forwards to Work’s experience section, with a normal fallback link.

Both [Anthropic](https://www.anthropic.com/) and [Jonathan Manta](https://jonathanmanta.com/) were inspected in the browser, including rendered screenshots and computed typography. The implementation borrows visual restraint and optional depth, without their branding, type assets, text, or layouts.

## Preservation

Work continued on `redesign/editorial-portfolio` from the existing `93b7d6a` commit. The working tree was clean at the initial inspection. The prior implementation and source assets remain in Git history; no reset, stash, rebase, branch deletion, or main-branch modification was used.

The source sweater portrait was replaced outside these implementation edits during the session. That change and a newly added image asset were preserved and left outside the revision commit. The optimized portrait derivatives were refreshed from the current supplied source. The résumé and suit portrait were unchanged. The historical [first-redesign report](./redesign-review.md) remains available and is explicitly marked as historical.

The updated responsive portrait files are 320 × 400 (6,654 bytes) and 640 × 800 (34,730 bytes). HTML declares the dimensions and responsive source sizes. The primary portrait is eagerly loaded; there are no separate below-the-fold image assets. No room-reference image is shipped as part of the design.

## Rendered review and accessibility

Reviewed all nine content pages in desktop and phone screenshots, including the Work page with its disclosures expanded. After that review, refined the homepage’s paragraph wrapping and gave the professional disclosures distinct descriptive labels. Rechecked Home and Work after those changes.

- Desktop: 1440 × 900. Phone: 390 × 844. Home also fits within 1366 × 768, including its footer.
- Zero axe-core violations across the nine pages at both primary viewports under WCAG 2 A/AA, WCAG 2.1 AA, and best-practice rules. Expanded Work disclosures passed too.
- Every visible link and disclosure was checked for keyboard tab order and a visible focus outline. Skip links transfer focus to main content.
- Nineteen distinct local link/fragment targets returned successfully. The résumé returned HTTP 200, the PDF content type, and a valid `%PDF` signature.
- Home → Notes → first note → Work → uScheme navigation worked with JavaScript disabled. Native Work disclosures opened from the keyboard with JavaScript disabled. The old About URL forwarded correctly.
- All pages were checked at widths 320, 375, 390, 640, 768, 1024, and 1440 pixels, and with 200% text at a 640-pixel viewport. No horizontal overflow was detected.
- Images loaded with explicit dimensions. No failed resources or page errors were observed. Content pages include no JavaScript and make no external font or resource requests.
- The homepage scrolls naturally on phones; no content is clipped to make it fit.
- `git diff --check` passed.

The browser checks cover Chrome on this machine. Automated accessibility checks do not constitute a full accessibility certification. Screen-reader, Safari, Firefox, and real-device testing were not performed.

## Performance: this revision

Lighthouse 13.6.0 with headless Chrome 157 on Windows. Both versions were served by the same local Python HTTP server. “Before” is the existing editorial redesign at the start of this revision, not the original long portfolio. Values below are medians of three navigation runs per version and device, using matching simulated network/CPU settings. Final measurements ran after the layout/accessibility audits stopped.

| Lab metric | Mobile before | Mobile after | Desktop before | Desktop after |
| --- | ---: | ---: | ---: | ---: |
| Performance score | 100 | 100 | 100 | 100 |
| LCP | 0.907 s | 0.756 s | 0.247 s | 0.204 s |
| CLS | 0 | 0 | 0 | 0 |
| Total blocking time | 0 ms | 1.6 ms | 0 ms | 0 ms |
| Transferred bytes | 18,436 | 18,864 | 18,436 | 18,864 |

Mobile: 390 × 844 CSS pixels, device scale factor 1, 150 ms RTT, 1,638.4 Kbps throughput, and 4× CPU slowdown. Desktop: 1440 × 900, device scale factor 1, 40 ms RTT, 10,240 Kbps throughput, and 1× CPU. Lighthouse storage reset was enabled. Transfer totals reflect this local server rather than production compression or caching; higher-density devices may select the larger portrait.

Mobile LCP ranged from 0.904–0.910 s before and 0.753–0.773 s after. Desktop LCP ranged from 0.245–0.443 s before and 0.203–0.205 s after. One baseline desktop run scored 84, with 372.5 ms blocking time and 0.0176 CLS; it remains in the three-run sample rather than being discarded. All six final runs scored 100, with CLS 0. The transfer increase was 428 bytes, approximately 2.3%.

These are small local lab samples. The observed LCP values are comfortably below 2.5 s, and CLS is below 0.1. They do not establish real-user performance or a guaranteed production speedup. INP was not measured; navigation-only Lighthouse results and total blocking time are not substitutes for an interaction distribution. Real-user LCP, CLS, and INP remain unmeasured.

## Review status

This revision and the first note remain unpublished on the dedicated redesign branch. No push, merge, or deployment was performed for this revision. The local preview is available for review.
