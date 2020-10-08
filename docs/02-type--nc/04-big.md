## big integer/number

```
0x1234N
```

equal

```
bignum #[2 u8!][0x34u8 0x12u8]
```

type: `[bignum! [2 u8!]]`

```
-1234N
```

equal

```
-bigint #[2 u8!][0xD2u8 0x04u8]
```

type: `[bigint! [2 u8!]]`

### declare

```
declare a [bigint! [2 u8!]]
declare a [* [bigint! [2 u8!]]]
```
