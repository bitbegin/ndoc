## function

### func

```
f: func [a [integer!] b [integer!] return: [integer!]][a + b]
a: #[function! [a [integer!] b [integer!] return: [integer!]]] null
a: :f
```

### extension

```
#inline
#variadic
#cdecl
#stdcall
```

### print format

```
;-- hex
/x
/04x
;-- float
/f
;-- unicode 16
/u16
;-- 16B align
/b
/16b
;-- 4x4 align pointer
/p
/4p
;-- unicode 16 string
/u

a: #[char! 32][]

print [/b a]

print [/p a]
```

### named parameters

```
f: func [x [integer!] y [integer!] -> [integer!]][x + y]

f #(y: 2 x: 1)
```

### default parameters

```
f: func [x [integer!] = 0 y [integer!] -> [integer!]][x + y]

f #(y: 2)
```

### scope variable in function

```
f: function [x [integer!] = 0 y [integer!] = 2 -> [integer!]][
	do [
		local z: [integer!] 3
		x + y + z
	]
]

f 1 3
```
