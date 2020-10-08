## string

just pointers

### cstring! (utf8, 1byte)

similar to `* char!`

```
cstring "string"
```


### wstring! (unicode 16, 2byte)

similar to `* u16!`

```
wstring "string"
```

### string! (unicode, 4byte)

similar to `* u32!`

```
string "string"
```

### multi line string

```
cstring {string}
cstring %%{raw string}%% 
```

### notes: lexer string is like a array pointer

```
"this is a string!"
```

eq.

```
* #[] "this is a string!"
```
