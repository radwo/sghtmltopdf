A run raised or lowered with `vertical-align` (`middle`, `sub`, a length and so on) now grows
the line only as far as its `line-height` tall box sticks out, as browsers do. Under a
`line-height` smaller than the font's ascent plus descent (Bootstrap sets 16px on 14px table
cells) every such line came out about 2px taller than in Chrome, and under a larger
`line-height` the run did not grow the line at all.
