## pointer

`*` = `pointer`

```
const * * u8! = const pointer pointer u8!

declare a [u32]
declare p1 [* u32!] = :a
declare p2 [* * u32!] = :p1
p2/0/0: 3U

poke pick p2 0 0 3U

print-line a
;-- 3 

;-- or
p1/0: 3U 
```
