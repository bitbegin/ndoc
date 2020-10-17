## string

just pointers

### utf8, 1byte

type: `#[6 char!]`

```
s1: stack #[char! 6] #utf8 "hello"
s2: #[char! 6] #utf8 "hello"
s3: #utf8 "hello"

s4: [#'h' #'e' #'l' #'l' #'o' #'']
```

type: `#[pointer! [6 char!]]`

```
s1: #[pointer! [char! 6]] pointer stack #utf8 "hello"
s2: #[pointer! [char! 6]] pointer #utf8 "hello"
s3: pointer #utf8 "hello"

s4: pointer [#'h' #'e' #'l' #'l' #'o' #'']
```

type: `#[pointer! char!]`

```
a: #[pointer! char!] pointer #utf8 "hello"
```

### unicode 16, 2byte

type: `#[6 u16!]`

```
#u16 "string"
```

### unicode, 4byte

type: `#[6 uchar!]`

```
s1: #[uchar! 6] stack "hello"
s2: #[uchar! 6] "hello"
s3: "hello"

s4: [#"h" #"e" #"l" #"l" #"o" #""]
```

type: `#[pointer! [6 uchar!]]`

```
s1: #[pointer! [uchar! 6]] pointer stack "hello"
s2: #[pointer! [uchar! 6]] pointer "hello"
s3: pointer "hello"

s4: pointer [#"h" #"e" #"l" #"l" #"o" #""]
```

type: `#[pointer! uchar!]`

```
a: #[pointer! uchar!] pointer "hello"
```

### multi line string

```
{string}
%%{raw string}%%
```
