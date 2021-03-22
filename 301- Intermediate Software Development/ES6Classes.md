# ES6 Classes

Clases are a template for creting objects. In Javascript Classes are built on [prototypes](https://www.w3schools.com/js/js_object_prototypes.asp). Classes are "Special Functions," which can be defined similarly to how you would define a function, i.e a class can have both an expression and a declarations.

## Declaring a Class

To declare a class, you use the `class` keyword. For example:

``` JS
class Music{
  constructor(genre, artiste) {
    this.genre = genre;
    this.artiste = artiste;
  }
}
```

## Class Expressions

This is another way to define a class. Class expressions can be named or unnamed. For eg:

```JS
let Music = class{
  constructor(genre, artiste) {
    this.genre = genre;
    this.artiste = artiste;
  }
}
```

References:

[Developer Mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
