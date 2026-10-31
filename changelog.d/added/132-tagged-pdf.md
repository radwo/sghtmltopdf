`--tagged` (`tagged: true` in the Ruby gem, `?tagged` on the server) writes a tagged PDF
(#132). It adds a structure tree for screen readers and other assistive technology:
headings (`H1` to `H6`), paragraphs, lists (`L`, `LI`, `Lbl`, `LBody`), tables (`Table`,
`THead`/`TBody`/`TFoot`, `TR`, `TH` with `Scope`, `TD`, spans, `Caption`), links (each with its
annotation) and images with an `alt` as `Figure`s carrying it. Backgrounds, borders, headers,
footers, a `<thead>` repeated on a later page and an `<img>` without `alt` are marked as
artifacts. `--streaming` does not support it.

Two known limitations of the structure tree: it follows paint order, not DOM order, so floats
and `z-index` can reorder it (an `H2` before the `Div > H1` it follows in the HTML); and a link
around an image gets a `Link` element of its own at the end of the document, as a sibling of the
`Figure`, instead of one that wraps it.
