## mod/import

```
;-- file1.bc

a: 1
_b: 2
c: context [
  x: 1
  y: 2
]
```

```
import %file1.bc [a c c/x c/y]

import %file1.bc [c []] ;-- c/x c/y

import std []
```
