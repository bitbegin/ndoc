## dynamic

```
dyn [_ a [int!] b [int!]] dyn-test


;-- print
dyn [_] dyn-print
impl print: dyn-print [self [integer!]][]

impl print: dyn-print [#variadic count [int!] list [* token!]][] 
```
