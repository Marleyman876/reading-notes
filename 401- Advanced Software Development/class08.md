# List Comprehensions in Python

The list comprehension always returns a result list.

If you used to do it like this:

```py
new_list = []
for i in old_list:
    if filter(i):
        new_list.append(expressions(i))
```

You can obtain the same thing using list comprehension. Notice the append method has vanished!

```py
new_list = [expression(i) for i in old_list if filter(i)]
```

## Benefits of Using List Comprehension

* It’s a single tool that you can use in many different situations

* In addition to standard list creation, list comprehensions can also be used for mapping and filtering

* List comprehensions are also more declarative than loops, which means they’re easier to read and understand. Loops require you to focus on how the list is created
