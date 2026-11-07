# Kindle Lab test books

Small EPUBs that each test one thing a Kindle does with a personal document sent through Send to Kindle.
Amazon converts every EPUB you send (to KFX), and the device shows the conversion, not your file, so a
desktop reader cannot tell you what the Kindle will do. Only the device can.

Results, as a table of features by devices: **https://dropkind.app/kindle-lab**

The same results as data: [`kindle-lab.json`](kindle-lab.json) (a copy of
https://dropkind.app/kindle-lab.json, which is always current).

| Book | What it checks |
|---|---|
| `books/kindle-lab-menclose-longdiv.epub` | Whether one MathML `menclose notation="longdiv"` turns the whole book into a fixed page (no font size). On a Paperwhite 2024, firmware 5.20.1, it does. |
| `books/kindle-lab-menclose-default.epub` | The same with a bare `menclose`: MathML makes long division the default, so it locks the book too. |
| `books/kindle-lab-menclose-box.epub` | `menclose notation="box"`: the frame is drawn and the book reflows. |
| `books/kindle-lab-menclose-control.epub` | The control: the same book with `mrow`. Send it the same way as the others and compare the font size. |
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

The books and the results are CC0: use them for anything. They are built by [DropKind](https://dropkind.app), which
sends articles, PDFs and papers to Kindle and applies the workarounds found here.
