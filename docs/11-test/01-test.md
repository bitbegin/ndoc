## test

### single test

```
test "test name" [
	a: 1
	b: 2
	assert a = b
]
```

### group tests

```
tests "group name" [
	test "test name" [
		a: 1
		b: 2
		assert a = b
	]
]
```
