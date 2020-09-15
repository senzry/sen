***※under construction***

# 🪑 type description reference
type can be used primarily for the following applications
- Pre-transmission validation
- Data validation with some sen editor
  - Verification rules used in the UI implemented in browsers and other devices
- Interface Description

## ✔ type define operator ":@ <"
```sen
:@Book<
```
The definition of type begins with ":@" and ends with "<".  
with name-fixing operator "$"  
```sen
:@$Book<
```
In addition, the beginning ":" is a meta-description operator.

### ◆ property additions operator ">"
```sen
:@Book
  >title
<
```
with name-fixing operator "$"  
```sen
:@$Book
  >$title
<
```

### ◆ type designation operator "@"
```sen
:@Book
  >title @string
<
```
You can specify the type of the property by specifying a type token.  
// TODO type token  
// TODO type-determining expression  

### ◆ doc-comment operator "!"
Doc comment Operator "!" to write a comment is available.    
It is possible to write a value literal afterwards.  

## 🧩 type expression

### ◆ type alies operator "="
```sen
:@Book = string<
```
### ◆ type wrap operator "-"
```sen
>foo@listof - nullable - string

//"Another way to write"
>foo@listof<nullable<string>>
>foo@list<nullable<string>> - nullable - string

```

### ◆ type sum operator "|"
```sen
>foo@string | number | "FOO"

//"Another way to write"
>foo@listof<nullable<string>>
>foo@list<nullable<string>> - nullable - string

```



## ◆ // TODO 

```sen
:@ Book
  >title @string
  >price @nullable - number
  >auther @ :@Human
    >name @string
    >birthdate @date
    >gender @nullable - :@Gender = "male" | "female" | "other" <
  <
<
```



