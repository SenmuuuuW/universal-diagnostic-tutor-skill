# Source Refresh Maintenance

Use this guidance when maintaining source packs. Keep the packs lightweight,
current enough to be useful, and honest about stale or unverified links.

## Refresh Cadence

- Check source packs after each release that changes resource behavior.
- Recheck term-specific course links at least before major version releases.
- Recheck any source marked stale, unverified, or term-specific before citing it
  in an answer.
- Do not run broad scraping or download course archives. Use lightweight page
  reachability checks and manual review.

## How To Mark Link State

Use the `Caution` field in source entries:

- `Term-specific page; verify current term before citing.`
- `Unverified in this environment; verify before citing.`
- `Stale link candidate; replace with a current official page when available.`
- `Broad homepage; prefer a specific lecture, assignment, or section page when
  possible.`

Do not silently keep broken links. Either replace the link, mark it clearly, or
omit the source.

## Replacing Term-Specific Pages

When replacing a course page:

1. Prefer the same institution and course if the current public term is
   available.
2. Prefer stable course landing pages over short-lived semester pages when both
   are equally useful.
3. Preserve the source's teaching role: beginner overview, formal course,
   assignment, standard, or official documentation.
4. Update the `Caution` field if the new page is still term-specific.
5. Mention the source change in the release summary or changelog when
   user-visible.

## Avoid Source Rot

- Prefer official documentation and stable university/open textbook pages.
- Avoid random mirrors, unofficial textbook uploads, and copied PDFs.
- Avoid answer-only sites that are likely to disappear or encourage memorizing.
- Keep broad homepages only when they are the best stable entry point.
- Prefer exact pages for claims, assignments, lectures, standards, and docs.

## Keep Packs Lightweight

- Add source metadata and usage notes only.
- Do not copy lecture content, textbook passages, problem statements, or answer
  keys.
- Keep each pack curated. A few strong sources are better than many weak links.
- Remove redundant sources when a better source already covers the same role.

## Maintenance Report Format

When reporting source-pack maintenance, include:

- Sources added.
- Sources removed or replaced.
- Links marked stale, unverified, or term-specific.
- Any source areas still undercovered.
- Confirmation that no copied copyrighted material, PDFs, secrets, scripts, or
  package setup were added.
