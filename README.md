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

## PDF reference sheets — one single sheet per framework
Each framework's "View Full A4 Reference Sheet" button opens a PDF containing **only that
one framework's sheet** — students see a single page, nothing else. The 140 files live in
the `sheets/` subfolder, named by title slug (e.g. `sheets/dikw-pyramid.pdf`,
`sheets/modern-portfolio-theory.pdf`).

## Sheet viewer (MARTI301-style, with Search PDF)
The viewer renders each sheet with PDF.js and includes a toolbar: a **Search PDF** box
(with match count and prev/next arrows), zoom −/+, open-in-new-tab, and close. PDF.js is
loaded from a CDN (cdnjs) via two `<script type="module">` references already in each page —
no extra files to upload, but the viewer needs internet access to load the library (which
any student browser has). Search works across the whole sheet even though the source PDF
splits text into single characters.

**Deploy:** upload the `sheets/` folder (all 140 PDFs) alongside the HTML files, keeping the
folder name `sheets`. It must sit in the same directory as the unit pages and `gallery.html`.

## Notes
- All popup content (definitions, key points, references) is authored for teaching;
  well-known frameworks carry curated Harvard references, others a Thumbnail-Thinking source.
- © 2026 Dr. Hildegard Haas · EU Business School. Applies JD Meier's *Thumbnail Thinking*
  & *Council of Giants*; core messages after Bostelaar.
