## const

**variable can't be changed**

```
const a: static "this is a string!"
const a: #[pointer! uchar!] static "this is a string!"
```

**the pointer value can't be changed**

```
a: const static "this is a string!"
a: const #[pointer! uchar!] static "this is a string!"
```

**both can't be changed**
```
const a: const static "this is a string!"
const a: #[const pointer! uchar!] static "this is a string!"
```

### examples

**variable can't be changed**

```
b: #[integer!] 0
const a: #[pointer! integer!] :b
```

**the pointer value can't be changed**

```
b: 3
a: #[const pointer! integer!] null
a: :b
;-- but below will compile with failure
a/1: 4
```

**both can't be changed**

```
b: #[integer!] 3
const a: #[const pointer! integer!] :b
```
