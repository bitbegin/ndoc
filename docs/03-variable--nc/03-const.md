## const

**variable can't be changed**

```
a: const cstring "this is a string!"
```

**the pointer value can't be changed**

```
const a: cstring "this is a string!"
```

**both can't be changed**
```
const a: const cstring "this is a string!"
```

### examples

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
