***※under construction***

# 👀 Comparison with JSON
Let's get acquainted with sen's notation in comparison to JSON, a popular notation.
## Basic usage
To represent a simple single object in a text file, it is written as follows.

```JSON
・JSON

{
  "title": "Rainbow Fish",
  "code": "978-3-3140-1544-1",
  "genre": "Children's book",
  "issueDate": "1992-01-27",
  "author": {
    "name": "Marcus Pfister",
    "birthdate": "1960-07-30"
  },
  "dailySales": 2,
  "isOutOfPrint": false
}
```
```sen
・sen

>title : "Rainbow Fish"
>code : "978-3-3140-1544-1"
>genre : "Children's book"
>issueDate : 1992-01-27
>author :
  >name : "Marcus Pfister"
  >birthdate : 1960-07-30
<
>dailySales : 2
>isOutOfPrint : false
```
They are similar but not the same. Let's check out what's going on, one by one.
### Flat
It's not a big deal, but it doesn't require a root object like Json.  
If you need a root object, write the following.
```sen
>:
  >title : "Rainbow Fish"
  >code : "978-3-3140-1544-1"
  >genre : "Children's book"
  >issueDate : 1992-01-27
  >author :
    >name : "Marcus Pfister"
    >birthdate : 1960-07-30
  <
  >dailySales : 2
  >isOutOfPrint : false
<
```
### String
String in sen is simple and straightforward.  
- Surrounded by double or back quotations.  
- Quotation marks escape by layering them on top of each other.  

The sen string can contain all possible characters without escaping.  
```sen
>title : "Rainbow Fish"
>code : "978-3-3140-1544-1"
>remarks: "This book is a hot seller.
Please stack it as flat as possible."
```
Hence, each application layer may require its own sanitization.  
The basic encoding is UTF8. There is a way to describe the encoding hints is provided.  
### Property name is not a string
For example, the following property names are allowed in JSON.  
```JSON
{
  "number": 1,
  "text": "string",
  "bool": true,
  "null": null,
  "": 1,
  " ": 1,
  "foo bar": 1,
  "1": 1,
  "-1": -1,
  "\n": 1,
  "\t": 1,
  "\\": 1,
  "/foo": 1,
  "\u0001": 1
}
```
This is because JSON objects are key-value, not structures.  
Key-value is easy to understand, but it's unwieldy from programs that need the type.  
(Strictly speaking, JSON is not a pure key-value because it allows for key duplication.)  
In sen, the only available symbol for a property name is the underscore. (Only the underscore is an error.)  
Property names must be written in alphanumeric form only and must not contain spaces or begin with a number.  
### Comment

// TODO





