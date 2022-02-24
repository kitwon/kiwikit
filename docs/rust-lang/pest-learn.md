---
tags: rust pest grammar-parser ast
---

# Pest Learn

Pest is a **grammar parser**, it uses [parsing exprssion gammar.](https://en.wikipedia.org/wiki/Parsing_expression_grammar) as input.

> Docs -- https://pest.rs/book/intro.html
> Grammars syntax -- https://pest.rs/book/grammars/syntax.html

## Pest file

```
field = { (ASCII_DIGIT | "." | "-")+ }
record = { field ~ ("," ~ field)* }
file = { SOI ~ (record ~ ("\r\n" | "\n"))* ~ EOI }
```

1. At line 1. In this code block, pest define a **Rule (Statement)** call `field`. This is description for every number field: each character is either an ASCII digit `0` throuth `9`, a full stop sign `.` or a hyper-minus `-`. The plus sign `+` indicates that the pattern can repeat on or more times.
2. At line 2. The tilde `~` means **"and then"**, for example field1 is `123` and field is `567`, so that `field1 ~ field2` is matches `123` follow by `567` (For this grammar `123 ~ 567` is exactly the same as `123567`).
3. The asterisk is just like #regex, repeat **zero or more**.
4. At line 3. There are two special rules `SOI (Start of input))` and `EOI (End of input)` that match. Without `EOI`, **the `file` would just stop as soon as it found the first invalid character and report a successful parse**