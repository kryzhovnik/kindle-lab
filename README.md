# Kindle Lab test books

Small EPUBs that each test one thing a Kindle does with a personal document sent through Send to Kindle.
Amazon converts every EPUB you send (to KFX), and the device shows the conversion, not your file, so a
desktop reader cannot tell you what the Kindle will do. Only the device can.

Results and the full write-up: **https://dropkind.app/kindle-lab**

| Book | What it checks |
|---|---|
| `books/kindle-lab-menclose.epub` + `books/kindle-lab-menclose-control.epub` | Whether one MathML `menclose` turns the whole book into a fixed page (no font size). Send both the same way and compare. |
| `books/kindle-lab-mathml-elements.epub` | Which documented MathML elements render, one numbered case each. |
| `books/kindle-lab-footnotes.epub` | How much of a two-paragraph note the pop-up shows, for six markups. |
| `books/kindle-lab-full-page-cover.epub` | A full-page picture as an SVG box versus an `img`. |
| `books/kindle-lab-title-from-filename.epub` | Whether the library shows the file name or the `dc:title`. |

Each book says on its first page what a correct result looks like.

## Report a result

Open an issue with the "Device report" template: Kindle model, firmware (Settings → Device Options →
Device Info), Amazon region, how you sent the book (email, Send to Kindle app/web, another tool), and
what you saw. A photo helps. A failure is as useful as a pass; reports are added to the table on the page.

## Licence

The books are CC0: use them for anything. They are built by [DropKind](https://dropkind.app), which
sends articles, PDFs and papers to Kindle and applies the workarounds found here.
