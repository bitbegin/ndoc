## array pointer

```
[1 2 3 4]
```

eq.

```
* #[][1 2 3 4]
```

### declare

```
declare a [* #[4 int!]]
declare a [* [array! [4 int!]]]
```

### slice

```
a: [1 2 3 4]
s: 0 .. 3		;-- int! x int!
b: a/s

;-- type? b = * #[3 int!]

```
