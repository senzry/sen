***※under construction***

# 💎 Object description reference

## ✔ let operator ">"
Define values by using sub-operators until the next let operator.
```sen
>foo
```
The let operator must be immediately followed by a name-token, for example "foo".  
If a type is specified, it describes the value to be set for the corresponding property.  
See //TODO expanded notation.  
The sub-operators of let are described below.  

### ◆ name-fixing operator "$"
The following notation I just showed you was actually a shorthand notation.
```sen
>foo
```
Without abbreviating the above, it looks like this

```sen
>$foo
```

### ◆ name token
Name token is used to describe the property name.  
For ease of migration between systems, the following rules exist.  
In sen, the only available name-token for a property name is the underscore. (Only the underscore is an error.)  
Name token must be written in alphanumeric form only and must not contain spaces or begin with a number.  

### ◆ value operator ":"
```sen
>foo:"bar"
```
The value operator ":" is used to describe the value specified for the property. 
It is immediately followed by a value literal such as "bar".  
//TODO value literal

### ◆ comment operator "//"
```sen
//"comment"
>foo//"comment":"bar"//"comment"
//"comment"
```
With a few exceptions, you can write comments in all sorts of places.  
You may or may not write a value literal behind the comment operator.  


### ◆ type designation operator "@"
```sen
>foo@string:"bar"
```
You can specify the type of the property by specifying a type token.  
// TODO type token  
// TODO type-determining expression  
Sen ignores any whitespace that is unnecessarily sandwiched in between, so you can format it for better viewing.  
Furthermore, let descriptions are in no order.  
It is also possible to write from a type definition.  
```sen
> @ string 
  $foo :"bar"
```
Eventually it will be minified and parsed.  
```sen
>@string$foo:"bar"
```

## ✏ nested object
// TODO
## ✏ anonymous object
// TODO



