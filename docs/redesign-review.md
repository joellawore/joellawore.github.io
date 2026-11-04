# Portfolio redesign review

Review date: November 4, 2026. Local preview: <http://127.0.0.1:4173/>.

## Implementation

- Warm ivory, near-black text, and a restrained rust accent; Georgia headings and system sans-serif body text.
- A compact [home page](../index.html), [Work](../work.html), [About](../about.html), and five [project studies](../projects/).
- Three selected projects: uScheme optimization, Tufts SIS Modern, and readability classification. Universal Machine and skin-lesion studies remain available under More work.
- Shared Work / About / Résumé navigation. Normal anchors work without JavaScript.
- Tufts education, Wabtec internships, teaching, and 2027 availability are stated explicitly. Personal details come from the current résumé.
- Project diagrams are conceptual HTML summaries, not screenshots or reproduced course implementations. Coursework source remains private.
- No framework, JavaScript, animation library, web font download, loading screen, or entrance animation.
- Responsive portrait derivatives: 320 × 400 WebP (6,654 bytes) and 640 × 800 WebP (18,526 bytes), with source selection, dimensions, and high fetch priority. No below-the-fold images are used.

## Preservation and provenance

Fetched upstream main before editing. The redesign branch, `redesign/editorial-portfolio`, started from `origin/main` at `651b41418dd8d1c895d831088dd1ed5fcc6a801c`. Existing feature and recovery branches were preserved.

The pre-existing modified [résumé](../assets/joel-lawore-resume.pdf) and both original headshots were left untouched. Their SHA-256 values were checked before and after implementation:

| Existing asset | SHA-256 |
| --- | --- |
| Résumé PDF | `74F0A7E38E0DB443DCA5CFD46EC94DE96CE50FCF921971B33B70041FBC2F5DAF` |
| Suit headshot | `8AFC6AC9C659EBC1DE95EC5551EBE3A576420EF0E95D3C187C825A4E1E962F8C` |
| Sweater headshot | `C9AFD43D4D22A7A89761A4C8D94E9FEDE7E65EBF5803AE259C6DD4D15198B608` |

Copy was checked against the previous portfolio and current résumé. The Wabtec AI evaluation framework and the intern challenge access-management pipeline are described as separate projects. No results, testimonials, source-code links, screenshots, or project demos were invented.

## Performance: lab measurements

Lighthouse 13.6.0, headless Chrome 157 on Windows. Both versions were served from the same local Python HTTP server. Values are medians of three navigation runs per device and version, with matching simulated network/CPU settings and storage reset. The final performance runs were collected after the layout/accessibility audits stopped.

| Lab metric | Mobile before | Mobile after | Desktop before | Desktop after |
| --- | ---: | ---: | ---: | ---: |
| Performance score | 100 | 100 | 100 | 100 |
| LCP | 1.013 s | 0.948 s | 0.282 s | 0.247 s |
| CLS | 0 | 0 | 0 | 0 |
| Total blocking time | 0 ms | 29 ms | 0 ms | 0 ms |
| Total transferred bytes | 36,245 | 18,436 | 36,245 | 18,436 |

Mobile emulation: 390 × 844 CSS pixels, device scale factor 1, 150 ms RTT, 1,638.4 Kbps throughput, and 4× CPU slowdown. Desktop emulation: 1440 × 900, device scale factor 1, 40 ms RTT, 10,240 Kbps throughput, and 1× CPU. Lighthouse used simulated throttling. Transfer values reflect this local server and its response headers, not production compression or caching.

Mobile LCP ranges: before 0.960–1.025 s; after 0.911–1.007 s. Desktop ranges: before 0.253–0.306 s; after 0.244–0.247 s. The modest timing differences fall within a small lab sample; the main outcomes are retaining fast rendering and reducing transfer by about 49%. The mobile blocking-time increase was 7.5–46 ms across final runs despite no site JavaScript; browser rendering work still contributes to this metric.

All sampled LCP and CLS values meet the requested 2.5 s and 0.1 targets. These are local lab results, not real-user measurements. INP was not established: navigation-only Lighthouse runs do not measure a representative interaction distribution. Total blocking time is a separate lab metric and is not an INP result. Production latency, caching, devices, and real-user LCP/CLS/INP remain to be measured after an approved deployment.

## Validation

- Rendered and visually reviewed all eight pages in desktop and mobile Chrome.
- Automated accessibility checks on all eight pages at 1440 × 900 and 390 × 844: zero axe-core violations under WCAG 2 A/AA, WCAG 2.1 AA, and best-practice rules. This includes text contrast; decorative rules are intentionally subtle.
- Checked keyboard tab order and visible focus on every link, plus skip-link visibility and transfer of focus to main content on every page.
- Checked 17 distinct local link/fragment targets, including the résumé's HTTP 200 response, PDF content type, and `%PDF` signature.
- Navigated Home → Work → uScheme → About with JavaScript disabled.
- Checked responsive image loading and explicit dimensions; no page, resource, or script errors.
- Checked all pages for horizontal overflow at widths 320, 375, 390, 640, 768, 1024, and 1440 pixels.
- Checked 200% text resizing at a 640-pixel viewport. No horizontal overflow or hidden content.
- The desktop home fits within 1440 × 900. Mobile scrolls naturally; no content is hidden to force a screen-height layout.
- `git diff --check` passed.

Validation covers Chrome on this machine. Automated accessibility checks do not replace a screen-reader review; Safari, Firefox, and real-device testing were not run.

## Review status

The redesign remains on its dedicated local branch. Main was not merged or changed by the redesign, and nothing was pushed or deployed. The original résumé change and raw portraits remain outside the redesign commit for the owner's separate review.
