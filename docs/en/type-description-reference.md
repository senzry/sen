***※under construction***

# 🪑 type description reference
type can be used primarily for the following applications
- Pre-transmission validation
- Data validation with some sen editor
  - Verification rules used in the UI implemented in browsers and other devices
- Interface Description
- scaffolding
It is incompatible with object notation to avoid complex and verbose notation.
## ✔ type define operator ":@ <"
```sen
:@Book<
```
The definition of type begins with ":@" and ends with "<".  
It is not necessary, but you can add $ as follows.  
```sen
:@$Book<
```
※The beginning ":" is a meta-description operator.

### ◆ property additions operator "> ;"
Let's add a title to the "Book".
```sen
:@Book
  >title;
<
```
with name-fixing operator "$"  
```sen
:@$Book
  >$title;
<
```
At first glance, the name-fixing operator may seem unnecessary.  
However, class names and property names do not necessarily need to be written at the beginning of the definition.  
```sen
:@
  >$title;
  $Book
<
```

#### ◆ type specification operator "@"
```sen
:@Book
  >title @string;
<
```
You can specify the type of the property by specifying a type token.  
// TODO type token  
// TODO type-determining expression  

### ◆ doc-comment operator "!"
Doc comment Operator "!" to write a comment is available.  
It is possible to write a value literal afterwards.  

// TODO

## ✔ type versioning operator "#"
Normally, type name duplication will result in an error, but different versions are allowed.
```sen
:@Book#0.1.0
  >title;
<
```

// TODO

## 🧩 type expression

### ◆ type alias operator "="
```sen
:@Book = string<
```
### ◆ type wrap operator "-"
```sen
>foo@listof - nullable - string;

//"Another way to write"
>foo@listof<nullable<string>>;
//"'listof' is an alias for 'list'."
>foo@list<nullable<string>>;

```

### ◆ type sum operator "|"
```sen
>foo@string | number | "FOO";
>bar@ "foo" | "bar" | "baz";
>baz@ 100 | 200 | 300;
```

## ◆ // TODO 

```sen
:@ Book
  >title @string;
  >price @nullable - number;
  >auther @ :@Human
    >name @string;
    >birthdate @date;
    >gender @nullable - :@Gender = "male" | "female" | "other" <;
  <;
<
```




