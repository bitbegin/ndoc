## scope

### before return or throw

```
f: func [][
	local p: #[int! 4] alloc [1 2 3 4]
	scope [p][free p]
	...
]
```
