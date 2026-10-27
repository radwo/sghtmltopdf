Embedded fonts are named after the font, with a subset tag, instead of `EmbeddedFont`.
`/BaseFont` and `/FontName` are now `ABCDEF+DMSans-Regular`: six uppercase letters derived
from the subset (so two subsets of one font differ, and the same input gives the same
names), a `+`, and the font's PostScript name, or its family and subfamily when it has none.
Preflight tools flagged the old names and PDF/A validators rejected them.
