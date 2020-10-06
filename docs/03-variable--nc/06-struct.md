## struct

```
type struct [
  a [integer!]
  b [integer!]
] struct-a

declare * struct-a! x: * struct-a [1 2]
```

### align

```
typedef struct [
  #align 4
  a [integer!]
  b [const * char!]
  c [8 char!]
] struct-b!
```
