`@supports` blocks are evaluated instead of always being dropped (#89).
`(property: value)` is true when the declaration parses (a `var()` value counts), `selector(...)`
when the selector parses, and `not`, `and`, `or` and parentheses combine them. Anything else,
such as `font-tech()` or an unknown function, is false. `@supports` nests with `@media` and
`@layer` in either direction.
