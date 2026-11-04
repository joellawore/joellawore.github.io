# Joel Lawore — personal website brief

Updated November 4, 2026. This brief supersedes the earlier recruiting-led portfolio direction wherever they conflict.

## Purpose

Make the site feel like Joel’s personal home on the web: a concise introduction, selected work, and room for occasional writing. Professional experience should be easy to find without making every page an application for a job. Be relaxed, thoughtful, curious, and concrete. Avoid slogans, exaggerated self-description, and invented personality.

## References and interpretation

- [Anthropic](https://www.anthropic.com/): inspected its current page, type styles, warm off-white ground, editorial hierarchy, and generous spacing. Borrow restraint and a clear reading rhythm, not the brand, proprietary fonts, corporate hero, or page layout.
- [Jonathan Manta](https://jonathanmanta.com/): inspected its concise introduction, narrow reading measure, personal interests, and native disclosure sections for optional depth. Borrow the ease of getting acquainted and choosing how much to read, not its text or composition.
- Joel’s supplied drawing-room images and references to the Charles Hotel in Cambridge and the Graduate Hotel in Princeton are mood references. Translate dark wood, books, leather, lamplight, and window light into warmth, color, and proportion. Do not use the images as page backgrounds or imply that Joel has visited either hotel.

## Visual direction

- Warm parchment background, deep brown text, muted brown secondary text, and one limited burgundy accent. Initial palette: parchment `#f5f0e6`, ink `#352a25`, secondary `#6b5b50`, burgundy `#713b46`, and subtle rules `#d8cdbd`. Confirm contrast in the rendered implementation.
- Readable Georgia headings with a system sans-serif body. Use comfortable body text, roughly 17–20 px, and generous line height. No external font request is necessary.
- A modest page width, shorter text measure, thin rules, and unembellished text links. Headings should introduce the content rather than dominate it.
- Keep the existing supplied portrait available, using the optimized responsive derivatives. The layout must also work without it. No generated or placeholder portraits.
- No literal textures, ornate frames, room-image backgrounds, gradients, floating cards, technology pills, decorative circles, offset shadows, proof-point panels, or entrance animation.

## Information architecture

### Shared navigation

Use **Home / Work / Notes** on every content page, with a visible current-page state and keyboard focus. Keep **Résumé** as a direct PDF link and **Email** as a mail link, visually quiet and easy to find in the shared footer. Preserve verified GitHub and LinkedIn links as secondary links.

### Home

- Plain introduction: Joel studies computer science and mathematics at Tufts.
- A short personal passage and a small “Lately” passage about music, drawn from supplied context. Use only a few interests, woven into prose. A natural mention of campus ministry is enough; no dedicated faith or values section.
- Link to a real note for optional depth. No empty feeds, placeholder articles, or invented reading/listening activity.
- Aim to fit comfortably on a typical desktop screen. On phones, short screens, or enlarged text, let the document scroll. Never clip, hide, or shrink essential content to meet a height target.
- No recruiting panel or repeated job-search copy.

### Work

- A selective overview of Wabtec experience, teaching at Tufts, and three strong projects: uScheme optimization, Tufts SIS Modern, and readability classification.
- Keep 2027 job availability to one understated mention on this page. Do not repeat it in metadata, project footers, or on Home and Notes.
- Use native disclosure elements where additional professional detail is useful. The summary should stand on its own.
- Keep benchmarks alongside the relevant project explanations, with the original evaluation context. Remove the benchmark from the overview.
- Preserve the existing Universal Machine and skin-lesion studies as optional depth rather than equal-weight selected work.
- No separate About or Values page. Migrate useful professional content from About to Work; an old About URL may forward to Work for compatibility.

### Notes

- Occasional short writing, initially one real draft based on the listening account supplied by Joel. No empty categories or promises of future posts.
- A compact Notes index and a standalone note with a comfortable reading measure.
- Mark the first note clearly as a draft for Joel’s review. The redesign and note remain unpublished pending review.
- Suggested first-note title: “I Want to Be Adored.” Retell the bus journey to New Jersey for his girlfriend’s album release, Spotify selecting the Stone Roses, recognition through exploring Manchester-related music and an interest in the Smiths, and his response to the opening noise, bassline, buildup, tension, and eerie vocals. End with imagining performing it.
- Do not add a date, concert, lyric, dialogue, relationship detail, musical observation, or personal experience not supplied by Joel. Do not add music history; if any historical claim becomes useful later, verify it independently and distinguish it from his listening experience.

### Project studies

Retain useful engineering explanations, accessible conceptual diagrams, results tables, and limitations. Coursework source stays private. Do not add fabricated demos, repositories, screenshots, achievements, metrics, or testimonials.

## Content and voice

The latest user message is the authority for personal context. The current résumé and existing verified project descriptions remain the basis for professional facts. Music is a substantial interest: listening closely, following connections, concerts, singing, and performing. Philosophy, Arsenal, intentional clothing and thrifting, and faith/campus ministry are available context, not a checklist to display.

Write in concise first-person prose. Warmth should come from specific, truthful details. Do not manufacture dry humor or turn interests into identity labels. Explain professional decisions plainly and keep original benchmark caveats. Distinguish Wabtec’s Salesforce evaluation work from the intern challenge access-management pipeline.

## Technical constraints

- Keep static HTML and shared CSS. No framework, animation library, or build step. Native links and disclosures work without JavaScript.
- Use system fonts; preserve responsive, optimized portrait assets, explicit dimensions, and useful alt text. Lazy-load future below-the-fold images. The room-reference images are not site assets.
- Preserve semantic headings, landmarks, skip links, visible focus, readable contrast, and meaningful link text.
- Never publish restricted coursework code or private authenticated screenshots.

## Implementation and review

1. Inspect status, branches, instructions, and the current changes before editing. Continue on `redesign/editorial-portfolio`; preserve existing commits, files, and unrelated work.
2. Update this brief before changing the implementation.
3. Implement Home / Work / Notes, move professional context to Work, update project navigation, and remove repeated availability messages.
4. Review rendered desktop and phone screenshots and revise visible problems. Check keyboard navigation, focus, contrast, internal links, résumé access, image loading, responsive widths, and enlarged text. Check navigation and disclosures without JavaScript.
5. Measure performance with the available browser tools and report actual settings and results. Aim for LCP under 2.5 s and CLS under 0.1; report INP only if a valid measurement is available. Lab results are not real-user metrics, and blocking time is not INP.
6. Provide a working local preview, a concise summary, and a validation report. Preserve the prior report as historical evidence and distinguish the current revision’s results.
7. Do not merge into main, push, or publish the redesign or note. Review can proceed from the local redesign branch.
