## function

### func

```
f: func [a [integer!] b [integer!] return: [integer!]][a + b]

f: func [a [integer!] b [integer!] return: [integer!]][a + b]
declare func [a [integer!] b [integer!] return: [integer!]] a
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
;-- string!
/s
;-- char
/c
;-- 16B align
/b
/16b
;-- 4x4 align pointer
/p
/4p
;-- unicode 16 string
/u

a: [32 char!][]

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
		declare z [integer!] = 3
		x + y + z
	]
]

f 1 3
```
