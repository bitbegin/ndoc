## mod/import

```
;-- file1.bc

pub a: 1
b: 2
pub c: context [
  pub x: 1
  pub y: 2
]
```

```
import %file1.bc [a c c/x c/y]

import %file1.bc [c []] ;-- c/x c/y

import std []
```
