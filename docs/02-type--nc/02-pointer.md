## pointer

### pointer = get address

```
a: pointer 3
```

### pointer!

```
x: #[pointer! [int!]] pointer 3
y: #[pointer! [int! 1]] pointer 3

z: pointer 3			;-- z = y
```

### null

```
a: #[pointer! [int!]] null
```

### access

```
p: pointer 1
p/0: 2
print pike p 0
poke p 0 3
```
