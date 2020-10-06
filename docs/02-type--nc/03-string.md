## string

### cstring! (utf8, 1byte)

```
cstring "string"
```


### wstring! (unicode 16, 2byte)

```
wstring "string"
```

### string! (unicode, 4byte)

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
* [] "this is a string!"
```
