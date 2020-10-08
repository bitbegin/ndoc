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

