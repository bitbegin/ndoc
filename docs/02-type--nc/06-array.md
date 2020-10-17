
## array

### value

#### base

type: `#[4 int!]`

```
d1: #[4 int!] stack [1 2 3 4]
e1: #[4 int!] alloc [1 2 3 4]
f1: #[4 int!] static [1 2 3 4]

d2: stack [1 2 3 4]
e2: alloc [1 2 3 4]
f2: static [1 2 3 4]

d3: [1 2 3 4]		;-- d3 = d1 = d2
```

#### string

type: `#[6 char!]`

```
s1: #[char! 6] stack #utf8 "hello"
s2: #[char! 6] #utf8 "hello"
s3: #utf8 "hello"

s4: [#'h' #'e' #'l' #'l' #'o' #'']
```

type: `#[uchar! 6]`

```
s1: #[uchar! 6] stack "hello"
s2: #[uchar! 6] "hello"
s3: "hello"

s4: [#"h" #"e" #"l" #"l" #"o" #""]
```

### pointer

#### base

```
d1: #[pointer [int! 4]] pointer stack [1 2 3 4]
e1: #[pointer [int! 4]] pointer alloc [1 2 3 4]
f1: #[pointer [int! 4]] pointer static [1 2 3 4]

d2: pointer stack [1 2 3 4]
e2: pointer alloc [1 2 3 4]
f2: pointer static [1 2 3 4]

d3: pointer [1 2 3 4]		;-- d3 = d1 = d2
```

```
a: [pointer int!] pointer stack #[1 2 3 4]
```

#### string

type: `#[pointer! [6 char!]]`

```
s1: #[pointer! [char! 6]] pointer stack #utf8 "hello"
s2: #[pointer! [char! 6]] pointer #utf8 "hello"
s3: pointer #utf8 "hello"

s4: pointer [#'h' #'e' #'l' #'l' #'o' #'']
```

```
a: #[pointer! [char!]] pointer stack #utf8 "hello"
```
