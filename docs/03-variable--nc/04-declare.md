## declare

```
declare integer! a
declare integer! a: 2 ;-- eq. a: 2
```

### local stack

```
;-- stack, can edit
declare cstring! a: cstring push "this is a string!"
;-- stack, can't edit
declare const cstring! a: const cstring push "this is a string!"

;-- static, can edit
declare cstring! a: cstring "this is a string!"
;-- static, can't edit
declare const cstring! a: const cstring "this is a string!"

;-- stack, can't change a's pointer, can edit
declare cstring! const a: cstring push "this is a string!"
;-- stack, can't change a's pointer, can't edit
declare const cstring! const a: const cstring push "this is a string!"

;-- static, can't change a's pointer, can edit
declare cstring! const a: cstring "this is a string!"
;-- static, can't change a's pointer, can't edit
declare const cstring! const a: const cstring "this is a string!"

;-- auto reference
declare a: cstring "this is a string!"
declare a: const cstring "this is a string!"
declare const a: cstring "this is a string!" 
declare const a: const cstring "this is a string!"  
```

### global

```
;-- declare like above, but the strings are in global static
declare cstring! a: cstring "this is a string!"
declare a: cstring "this is a string!"


;-- simple
;-- static, can edit
a: cstring "this is a string!"
```
