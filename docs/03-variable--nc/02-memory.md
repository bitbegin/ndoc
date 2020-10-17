## memory

### stack

#### base

```
a1: #[u8!] stack 0u8
a2: stack 0u8
a3: 0u8

;-- as
b1: #[u8!] stack as u8! 32
b2: stack as u8! 32
b3: as u8! 32
```

#### array

```
a1: #[int! 4] stack [1 2 3 4]
a2: stack [1 2 3 4]
a3: [1 2 3 4]

;-- as
b1: #[int! 4] stack as [int! 4] [1u8 2u8 3u8 4u8]
b2: stack as [int! 4] [1u8 2u8 3u8 4u8]
b3: as [int! 4] [1u8 2u8 3u8 4u8]
```

#### array pointer

```
a1: #[pointer! [int! 4]] pointer stack [1 2 3 4]
a2: pointer stack [1 2 3 4]
a3: pointer [1 2 3 4]

;-- as
b1: #[pointer! [int! 4]] pointer stack as [int! 4] [1u8 2u8 3u8 4u8]
b2: pointer stack as [int! 4] [1u8 2u8 3u8 4u8]
b3: pointer as [int! 4] [1u8 2u8 3u8 4u8]
```

#### bigint

```
a1: #[bignum! 2] stack as [] [0x34u8 0x12u8]
a2: #[bignum! 2] stack 0x1234N
a3: 0x1234N
```


### static

**global memory, can modify**

### alloc

**head memory**

need `import std/memory/alloc`
