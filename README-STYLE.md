# Style: two-column sidebar

A sticky cream/sand sidebar (260px) carries the photo (circular crop), name, title, affiliation links and the vertical nav (current page = `class="current"`); the white main column holds the page content at a ~65-character measure. On phones the sidebar becomes a compact top header with a small photo and a wrapping horizontal nav. Font: Lato from Google Fonts, falling back to the system sans stack. Colours: sidebar `#f4eee2`, text `#2b2a27`, muted teal accent `#2f7a72` for links, headings and the current nav item. All styling is in `style.css`; the HTML has no inline styles, IDs per entry, or scripts (except the email obfuscator on the home page).

To add a publication, copy this block into the right `<ul class="pubs">` (newest first) and edit the text. Links always come in the order `[link, pdf]`: **link** is the publisher's article page via `https://doi.org/<DOI>` (the arXiv abstract page for preprints), and **pdf** is the published PDF, normally a copy in `papers/`. Any extras (for example `supp_text`) go after the pdf.

```html
    <li>
      <span class="links">[<a href="https://doi.org/10.xxxx/your-doi">link</a>, <a href="papers/your-file.pdf">pdf</a>]</span>
      A. Author, B. Author, V. Itskov.
      <em>Title of the paper.</em>
      Journal Name, 12(3):100-120, 2027.
    </li>
```
