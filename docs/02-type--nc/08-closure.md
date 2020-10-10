## closure

```
f1: func [a [int!] b [int!] -> ![x [int!] y [int!] -> [int!]]][
	local z: [int!] a + b
	![x [int!] y [int!] -> [int!]][x + y * z]
]

b: f1 1 2
b 3 4

c: [![x [int!] y [int!] -> [int!]]] f1 2 2
c 3 4

d: [closure! [x [int!] y [int!] -> [int!]]] f1 2 3
d 3 4
```
