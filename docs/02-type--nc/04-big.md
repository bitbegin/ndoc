## big integer/number


### big number

```
b: 0x1234N
b: [bignum! 2] stack 0x1234N
b: [bignum! 2] stack #[0x34u8 0x12u8]
```

### big integer

type: `[bignum! #[2 u8!]]`

```
b: -1234N
b: [bigint! 2] stack -1234N
b: [bigint! 2] stack #[-1 0xD2u8 0x04u8]
```

type: `[bigint! #[2 u8!]]`

### pointer

```
b: pointer 0x1234N
b: [pointer! [bignum! 2]] pointer stack 0x1234N
b: [pointer! [bignum! 2]] pointer stack #[0x34u8 0x12u8]
```

```
b: pointer -1234N
b: [pointer! [bigint! 2]] pointer stack -1234N
b: [pointer! [bigint! 2]] pointer stack #[-1 0xD2u8 0x04u8]
```
