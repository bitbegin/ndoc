## function

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
