# Style: two-column sidebar

A sticky cream/sand sidebar (260px) carries the photo (circular crop), name, title, affiliation links and the vertical nav (current page = `class="current"`); the white main column holds the page content at a ~65-character measure. On phones the sidebar becomes a compact top header with a small photo and a wrapping horizontal nav. Font: Lato from Google Fonts, falling back to the system sans stack. Colours: sidebar `#f4eee2`, text `#2b2a27`, muted teal accent `#2f7a72` for links, headings and the current nav item. All styling is in `style.css`; the HTML has no inline styles, IDs per entry, or scripts (except the email obfuscator on the home page).

To add a publication, copy this row into the right `<table class="pubs">` (newest first) and edit it. Each row has two cells: the **links** and the reference itself. The links cell has one line per `lk-row`: the first is always **link** (the publisher's article page via `https://doi.org/<DOI>`; the arXiv abstract page for preprints) and **pdf** (the published PDF, normally a copy in `papers/`). Optional further lines: an extra such as `supp`, placed under pdf with `class="under-pdf"`, and **ask questions** (`class="wide"`, centred under both) for a paper that has an "Ask this paper" page `ask/<id>/`. Each line is exactly one line of the reference text high, so the links sit on the reference's lines.

```html
    <tr>
      <td class="lk">
        <span class="lk-row"><a href="https://doi.org/10.xxxx/your-doi">link</a><a href="papers/your-file.pdf">pdf</a></span>
        <!-- only if the paper has an ask page: -->
        <span class="lk-row"><a class="wide" href="ask/your-paper-id/" title="Ask an AI assistant questions about this paper">ask questions</a></span>
      </td>
      <td class="ref">
        A. Author, B. Author, V. Itskov.
        <em>Title of the paper.</em>
        Journal Name, 12(3):100-120, 2027.
      </td>
    </tr>
```
