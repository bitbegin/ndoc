---
sidebar: auto
---


## 1. Abstract

xxx

## 2. Syntax

### 2.1 delimiters

```
WHITESPACE | "[" | "]" | "(" | ")" | ";" | "{" | "\"" | "#(" | "![" | "#{" | EOI
```

### 2.2 literals

#### 2.2.1 integers

```
;-- signed integers
-1i8
-2i16
-3i32
-4i64
-5i128

;-- unsigned integers
1u8
2u16
3u32
4u64
5u128

;-- isize!/int! default
-123
123

;-- isize!/int! 
-123I

;-- usize!/uint!
456U

;-- hex format
0x1234
0x1234U
0x1234u8
0x1234u16
0x1234u32
0x1234u64
0x1234u128

;-- big integer!
-123456N
0x12345678N
```

#### 2.2.2 float

```
;-- f32!/float!
1.23f32
1.#NaNf32
1.#INFf32
+1.#INFf32
-1.#INFf32

;-- f64!/double!
1.23
1.23f64 
1.#NaN
1.#INF
+1.#INF
-1.#INF
1.#NaNf64
1.#INFf64
+1.#INFf64
-1.#INFf64
```

#### 2.2.3 char

```
;-- char!, 1byte
#'A'

;-- uchar!, 4byte
#"中"
```

#### 2.2.4 string

```
;-- cstring! (utf8, 1byte)
as cstring! "string"

;-- wstring! (unicode 16, 2byte)
as wstring! "string"

;-- string! (unicode, 4byte)
as string! "string"


;-- multi line string
as cstring! {string}
as cstring! %%{raw string}%% 

```

#### 2.2.5 binary

```
#{11223344}
```

#### 2.2.6 array

```
;-- value
[][1 2 3 4 5 6 7 8]
[8 u8!][1]
[2 u8!][1 2 3 4]

;-- pointer
[1u8 2u8 3u8 4u8 5u8 6u8 7u8 8u8]
```

### 2.3 variable

#### word

first: `'a'..'z' | 'A'..'Z' | "_"`
then: `'0'..'9' | "-" | "*" | "!" | "?" | "."`

#### special word

`% + - & | ~ // / << <= <> < >> >= > = ** * ?? _ ..`

### 2.4 type define

```
type integer! a!
```

###  2.5 declare

```
declare integer! a
declare integer! a: 2 ;-- eq. a: 2

;-- const
declare integer! const a: 3   ;-- eq. const a: 3
```

#### push

this will copy the source to stack

```
d: as cstring! push "this is a string!"
```

###  2.6 pointer

`*` = `pointer`

```
const * * u8! = const pointer pointer u8!

declare u32! a 
declare * u32! p1: :a
declare ** u32! p2: :p1
p2/value/value: 3U

print-line a
;-- 3 

;-- or
p1/0: 3U 
```

### 2.7 string

```
"this is a string!"     ;-- eq. * [] "this is a string!"
```

### 2.8 array

```
[] "hello" = [6 char!][#'h' #'e' #'l' #'l' #'o' #''] 
```

#### const

**variable can't be changed**

```
declare integer! b 
declare * integer! const a: :b
```

**the pointer value can't be changed**

```
declare integer! b: 3
declare const pointer integer! a
a: :b
;-- but below will compile with failure
a/1: 4
```

**both can't be changed**

```
declare integer! b: 3
declare const pointer integer! const a: :b
```

### 2.9 struct

```
type struct [
  a [integer!]
  b [integer!]
] struct-a! 

* struct-a! [1 2]
```

#### align

```
typedef struct [
  #align 4
  a [integer!]
  b [const * char!]
  c [8 char!]
] struct-b!
```

### 2.10 enum

```
type enum [
  RED: 0
  BLUE
] enum-a! 

enum-a!/RED
```

### 2.11 code

```
![x + y]

declare code! a: ![x + y]
```

### 2.12 function

```
f: func [a [integer!] b [integer!] return: [integer!]][a + b]

f: func [a [integer!] b [integer!] return: [integer!]][a + b]
declare func [a [integer!] b [integer!] return: [integer!]] a
a: :f
```

#### extension

```
#inline
#variadic
#cdecl
#stdcall
```

### 2.13 scope

```
do [
  declare integer! a: 0
]

while [

][
  declare
]

if  xx [
  declare
]

forever [
  declare
]

loop count [
  declare
] 

```

### 2.14 print format

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



## 3. mod/import

```
;-- file1.bc

a: 1
_b: 2
c: context [
  x: 1
  y: 2
]
```

```
import %file1.bc [a c c/x c/y]

import %file1.bc [c []] ;-- c/x c/y

import std []
```

## 4. dynamic

```
dyn [_ a [int!] b [int!]] dyn-test


;-- print
dyn [_] dyn-print
print: dyn-print [self [integer!]][]

print: dyn-print [#variadic count [int!] list [* token!]][] 
```


## 5. import c lib/dll

## 6. async/await

## 7. catch/throw

## 8. marco

## 9. core/std library