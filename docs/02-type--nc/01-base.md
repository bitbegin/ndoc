## base

### integers

#### signed integers

* i8!
* i16!
* i32!
* i64!
* i128!

```
-1i8
-2i16
-3i32
-4i64
-5i128
```

#### unsigned integers

* u8!
* u16!
* u32!
* u64!
* u128!

```
1u8
2u16
3u32
4u64
5u128
```

#### size integer

* isize!/int!/integer!
* usize!/uint!

```
;-- default(isize!/int!)
-123

;-- isize!/int!
-123I

;-- usize!/uint!
456U
```

#### hex format

```
0x1234
0x1234U
0x1234u8
0x1234u16
0x1234u32
0x1234u64
0x1234u128
```


### float

#### f32!/float!

```
1.23f32
1.#NaNf32
1.#INFf32
+1.#INFf32
-1.#INFf32
```

#### f64!/double!

```
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

### char

#### char!, 1byte

```
#'A'
```

#### uchar!, 4byte

```
#"中"
```

### variable

#### value

```
a1: #[u8!] stack 0u8
b1: #[u8!] alloc 0u8
c1: #[u8!] static 0u8

a2: stack 0u8
b2: alloc 0u8
c2: static 0u8

a3: 0u8		;-- a3 = a1 = a2
```

#### pointer

```
a1: #[pointer! [u8!]] pointer stack 0u8
b1: #[pointer! [u8!]] pointer alloc 0u8
c1: #[pointer! [u8!]] pointer static 0u8

a2: pointer stack 0u8
b2: pointer alloc 0u8
c2: pointer static 0u8

a3: pointer 0u8		;-- a3 = a1 = a2
```

null:

```
a: #[pointer! u8!] null
```