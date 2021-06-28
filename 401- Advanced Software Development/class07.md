# Functions: The Local Scope

The local scope or function scope is a Python scope created at function calls. Every time you call a function, you’re also creating a new local scope.

An example of this is:

```py
def square(base):
...     result = base ** 2
...     print(f'The square of {base} is: {result}')
...
square(10)
The square of 10 is: 100
result  # Isn't accessible from outside square()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    result
NameError: name 'result' is not defined
base  # Isn't accessible from outside square()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    base
NameError: name 'base' is not defined
square(20)
The square of 20 is: 400
```
