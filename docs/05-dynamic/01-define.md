## dynamic

```
dyn-test: dyn [_ a [int!] b [int!]]

;-- print
dyn-print: dyn [_ x]
print: dyn-print [self [integer!]][]

;-- add
dyn-add: dyn [a _ b]
+: dyn-add [a [int!] b [int!] -> [int!]][a + b]
```
