# Dunder Methods

- They are easy to recognize because they start and end with double underscores, for example **init** or **str**.

- Dunder methods let you emulate the behavior of built-in types

-To construct account objects from the Account class I need a constructor which in Python is the **init** dunder:

```py
To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:
```

- Object represenatation:

**repr**: The “official” string representation of an object. This is how you would make an object of the class. The goal of **repr** is to be unambiguous.

**str**: The “informal” or nicely printable string representation of an object. This is for the enduser.

- Iteration

```py
def __len__(self):
        return len(self._transactions)

    def __getitem__(self, position):
        return self._transactions[position]
```

- To iterate over transactions in reversed order you can implement the **reversed** special method
