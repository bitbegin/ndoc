## array pointer

```
[1 2 3 4]
```

eq.

```
* #[][1 2 3 4]
```

### slice

```
a: [1 2 3 4]
s: 0 .. 3		;-- int! x int!
b: a/s

;-- type? b = * #[3 int!]

```
