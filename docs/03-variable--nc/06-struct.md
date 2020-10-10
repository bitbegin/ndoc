## struct

```
struct-a!: struct [
	a [integer!]
	b [integer!]
]

struct-b!: struct [
	a [struct-a!]
	b [integer!]
]

a: [struct-a!] static #[1 2]
b: [struct-b!] stack #[[1 2] 3]
```

### align

```
struct-p!: struct [
	#align 4
	a [integer!]
	b [const pointer! char!]
	c [8 char!]
]
```
