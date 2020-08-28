***※under construction***

# 👀 Comparison with JSON
Let's get acquainted with sen's notation in comparison to JSON, a popular notation.
## Basic usage
Represent a book with json and sen, it looks like this.  

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

// TODO





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








