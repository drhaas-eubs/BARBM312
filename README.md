# BARBM312 — Interactive Framework Galleries (Unit 1–7)

Seven interactive framework-gallery pages styled exactly like the MARTI301 reference:
clickable framework cards → popup (definition, diagram, key points, Harvard reference)
→ **View Full A4 Reference Sheet** button that opens the matching page in the
140-sheet `BARBM312_Framework_Sheet_Library.pdf`.

## Files
- `unit1.html` … `unit7.html` — one interactive gallery per unit (20 frameworks each, 140 total).
- `gallery.html` — **Complete Gallery Wall**: all 140 frameworks on one page, with a live search box (filter by name, theme, set, or unit). Same popup + PDF-viewer behaviour as the unit pages.

## Copy / print protection
All 8 pages disable text selection, right-click, drag, copy/cut, and the Ctrl/Cmd+P / +S / +U / +C shortcuts; printing shows a "not available for printing" notice instead of the content. Note: these are deterrents against casual copying only — a browser must render content to display it, so a determined user can still screenshot or read source. This matches what the MARTI301 reference does; there is no way to make web content truly uncopyable.

## Linking it from your homepage
On your `index.html`, point the "All 140 Frameworks — Complete Gallery Wall" button at `gallery.html` (same folder).

## Deployment (GitHub Pages)
1. Place these seven HTML files in your `BARBM312` repo (e.g. at the repo root, alongside
   the existing `unit1.html`, or in a subfolder — see note below).
2. **Place `BARBM312_Framework_Sheet_Library.pdf` in the SAME folder as the HTML files.**
   The "View Full A4 Reference Sheet" button opens `BARBM312_Framework_Sheet_Library.pdf#page=N`
   relative to the page, so the PDF must sit beside it.
3. The "‹ Back to Course Overview" link points to `../index.html`. If you put these pages at
   the repo root (not a subfolder), change that link to `index.html`.

## PDF reference sheets — one combined library, jump to page (MARTI301 match)
Each framework's "View Full A4 Reference Sheet" button opens the single combined
`BARBM312_Framework_Sheet_Library.pdf` at that framework's page, using
`BARBM312_Framework_Sheet_Library.pdf#page=N` — the same approach MARTI301 uses.

The library is: cover = p.1, master index = pp.2–3, sheets start at p.4. So framework
*k* (1-based, in course order) is at **PDF page k + 3**:

| Unit | Frameworks | PDF pages |
|------|-----------|-----------|
| 1 | 20 | 4–23 |
| 2 | 20 | 24–43 |
| 3 | 20 | 44–63 |
| 4 | 20 | 64–83 |
| 5 | 20 | 84–103 |
| 6 | 20 | 104–123 |
| 7 | 20 | 124–143 |

**Deploy:** put `BARBM312_Framework_Sheet_Library.pdf` in the SAME folder as the HTML
files (repo root). If you ever regenerate the PDF with a different front-matter length,
update the `pdfPageFor()` offset in `build.js` (currently `index + 3`).

## Notes
- All popup content (definitions, key points, references) is authored for teaching;
  well-known frameworks carry curated Harvard references, others a Thumbnail-Thinking source.
- © 2026 Dr. Hildegard Haas · EU Business School. Applies JD Meier's *Thumbnail Thinking*
  & *Council of Giants*; core messages after Bostelaar.
