## pointer

### pointer = get address

```
:a
pointer a
pointer 3
pointer array [][1 2 3 4]
```

### pointer!

`*` = `pointer!`

```
declare x [const pointer! [pointer! u8!]]
declare x [const * * u8!]
```

### examples

```
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
