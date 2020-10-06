## identify

### word

allow chars: `'a'..'z' | 'A'..'Z' | "_" | "+" | "-" | "*" | "!" | "?" | "." | '0'..'9'`

`'0'..'9'` not allowed for first place

### special word

`% + - & | ~ // / << <= <> < >> >= > = ** * ?? _ ..`

### delimiters

```
WHITESPACE | "[" | "]" | "(" | ")" | ";" | "{" | "\"" | "#(" | "![" | "#{" | EOI
```

### inner/public variable

* inner variable begin with `_`, like `_a: 0`
* others are public
