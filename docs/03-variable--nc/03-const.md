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
declare b [integer!]
declare const a [* integer!] = :b
```

**the pointer value can't be changed**

```
declare b [integer!] = 3
declare const a [pointer integer!]
a: :b
;-- but below will compile with failure
a/1: 4
```

**both can't be changed**

```
declare b [integer!] = 3
declare const a [const pointer integer!] = :b
```
