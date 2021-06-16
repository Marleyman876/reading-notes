# Read & Write in Python

Once you open a file you will want to read or write to the file.

```py

* .read(size=-1) This reads from the file based on the number of size bytes. If no argument is passed or None or -1 is passed, then the entire file is read.

*.readline(size=-1) This reads at most size number of characters from the line. This continues to the end of the line and then wraps back around. If no argument is passed or None or -1 is passed, then the entire line (or rest of the line) is read.

*.readlines() This reads the remaining lines from the file object and returns them as a list.

```

Another example of opening a text to read the file in python can be done using the following method:

```py

with open('dog_breeds.txt', 'r') as reader:
     # Read & print the entire file
      print(reader.read())

```

You can also break down lines and read each line byte by byte for eg:

```py
with open('dog_breeds.txt', 'r') as reader:
    # Read & print the first 5 characters of the line 5 times
    print(reader.readline(5))
    # Notice that line is greater than the 5 chars and continues
    # down the line, reading 5 chars each time until the end of the
    # line and then "wraps" around
    print(reader.readline(5))
    print(reader.readline(5))
    print(reader.readline(5))
    print(reader.readline(5))
Pug

Jack
Russe
ll Te
rrier

```

## Exceptions

An Exception error is an error that occurs whenever syntactically correct Python code results in an error. The last line of the message indicated what type of exception error you ran into.

For Example:

```py
print( 0 / 0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero (error message)

```

## Raising an Exception

We can use raise to throw an exception if a condition occurs. The statement can be complemented with a custom exception.

For example:

```py
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))

THe output of this code will be: 

Traceback (most recent call last):
  File "<input>", line 4, in <module>
Exception: x should not exceed 5. The value of x was: 10

```

For more reading on Expetions and read and write please follow the links in the references:

References:

1. [Real Python - Python Exceptions: An Introduction](https://realpython.com/python-exceptions/#exceptions-versus-syntax-errors)

2. [Python Tutorial for beginners | Exception Handling](https://www.youtube.com/watch?v=6SPDvPK38tw)

3. [Reading and Writing Files in Python (Guide)](https://realpython.com/read-write-files-python/)
