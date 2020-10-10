## string

just pointers

### utf8, 1byte

type: `[6 char!]`

```
s1: [6 char!] stack #utf8 "hello"
s2: [6 char!] #utf8 "hello"
s3: #utf8 "hello"

s4: #[#'h' #'e' #'l' #'l' #'o' #'']
```

type: `[pointer! [6 char!]]`

```
s1: [pointer! [6 char!]] stack pointer #utf8 "hello"
s2: [pointer! [6 char!]] pointer #utf8 "hello"
s3: pointer #utf8 "hello"

s4: pointer #[#'h' #'e' #'l' #'l' #'o' #'']
```

type: `[pointer! char!]`

```
a: [pointer! char!] pointer #utf8 "hello"
```

### unicode 16, 2byte

type: `[6 u16!]`

```
#u16 "string"
```

### unicode, 4byte

type: `[6 uchar!]`

```
s1: [6 uchar!] stack "hello"
s2: [6 uchar!] "hello"
s3: "hello"

s4: #[#"h" #"e" #"l" #"l" #"o" #""]
```

type: `[pointer! [6 uchar!]]`

```
s1: [pointer! [6 uchar!]] stack pointer "hello"
s2: [pointer! [6 uchar!]] pointer "hello"
s3: pointer "hello"

s4: pointer #[#"h" #"e" #"l" #"l" #"o" #""]
```

type: `[pointer! uchar!]`

```
a: [pointer! uchar!] pointer "hello"
```

### multi line string

```
{string}
%%{raw string}%%
```
