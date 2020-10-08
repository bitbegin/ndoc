## macro

### no paremeters

```
#macro a: [++ "x + 7"]

a    ;-- expand to x + 7
```

### two paremeters

```
#macro a: func [x y][
	++ x
	++ " + "
	++ y
]

a    ;-- expand to x + y
```

### token list

```
#macro a: func [t #variadic][
	repeat [++ " push " ++ t ++ " " ++ .]
]

a x [1 2 3 4]
;-- expand:
push x 1
push x 2
push x 3
push x 4
```

