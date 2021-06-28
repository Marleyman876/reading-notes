# Functions: The Local Scope

The local scope or function scope is a Python scope created at function calls. Every time you call a function, you’re also creating a new local scope.By default, parameters and names that you assign inside a function exist only within the function or local scope associated with the function call. When the function returns, the local scope is destroyed and the names are forgotten.

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

Python creates a local scope containing the names base (an argument) and result (a local variable). After the first call to square(), base holds a value of 10 and result holds a value of 100. The second time, the local names will not remember the values that were stored in them the first time the function was called.

## Global Scope

From the moment you start a Python program, you’re in the global Python scope. Internally, Python turns your program’s main script into a module called __main__ to hold the main program’s execution. The namespace of this module is the main global scope of your program. Whenever you run a Python program or an interactive session like in the above code, the interpreter executes the code in the module or script that serves as an entry point to your program. This module or script is loaded with the special name, __main__. From this point on, you can say that your main global scope is the scope of __main__.
