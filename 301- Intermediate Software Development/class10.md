# JavaScript Call Stack

The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

# Last in First Out (LIFO)

At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

```
function firstFunction(){
  throw new Error('Stack Trace Error');
}

function secondFunction(){
  firstFunction();
}

function thirdFunction(){
  secondFunction();
}

thirdFunction();
```

# Javascript Errors && Debugging

### Reference errors

This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

```
console.log(foo) // Uncaught ReferenceError: foo is not defined.
```

Whatever you are using (var, let or const) the fix is as simple has declaring the variable before any declaration is made.

```
let foo;
foo = 'Hello'
```

### Syntax errors

I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

```
JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1
```

This can be solved by just fixing the syntax, in this case the object should be a JSON.

```
JSON.parse('{"foo":"bar"}')
```

Some syntax errors like sending a trailing comma when calling a function are handled without error by most recent browsers, but older ones you have to be careful.

### Range errors

Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

```
var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length
```

An array for instance cannot have a negative length, why would you mess with the array length? Some people use it to set an array to empty, something of the likes of:

```
var foo = [0, 0]
foo.length = foo.length - 2 // (or foo.length - foo.length)
foo // would log [] instead of [0, 0]
```

I prefer not to mutate my variables whenever possible (making them constants and not variables) but this is a method that is available and now you know it.

### Type errors

Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

```
var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined
```

This is probably the most frequent error in JS, trying to access a property/method thinking that bar is of the type object when in reality, since it hasn’t been declared yet, it’s undefined which doesn’t have any baz available.
The fix is simple, just make sure that bar exists before trying to access it, either by creating bar or by checking for undefined.

```
var foo = { bar: {} }
foo.bar.baz // undefined but you avoid the error
or
var foo = {}
if (typeof foo.bar !== 'undefined') {
  foo.bar.baz // this will never be executed while bar does not exist
}
```

There are also warnings, for instance telling you about a deprecated method, which can be found more frequently in firefox developer tools.

### References

* [JavaScript error messages && debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c). 

* [The JavaScript Call Stack - What It Is and Why It's Necessary](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)