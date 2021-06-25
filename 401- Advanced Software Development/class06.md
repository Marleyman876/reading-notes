# How to use the Random Module in Python

Random functions contains some usefeul functions such as:

## randinit - the randint function Randint accepts two parameters: a lowest and a highest number

```py
import random
print random.randint(0, 5)
This will output either 1, 2, 3, 4 or 5.
```

## Generate Random Floats

The random.random() method returns a random float number between 0.0 to 1.0. The function doesn't need any arguments.

```py
 import random
random.random()
0.645173684807533
```

## Generate Random Numbers within Range

The random.randrange() method returns a randomly selected element from the range created by the start, stop and step arguments. The value of start is 0 by default. Similarly, the value of step is 1 by default.

```py
 random.randrange(1, 10)
 2
random.randrange(1, 10, 2)
 5            
random.randrange(0, 101, 10)
 80

```

## Select Random Elements

The random.choice() method returns a randomly selected element from a non-empty sequence. An empty sequence as argument raises an IndexError.

```py
 import random
 random.choice('computer')
't'          
 random.choice([12,23,45,67,65,43])
45           
 random.choice((12,23,45,67,65,43))
67
Shuffle Elements Randomly

```

## The random.shuffle() method randomly reorders the elements in a list.

```py

 numbers=[12,23,45,67,65,43]
 random.shuffle(numbers)
 numbers
[23, 12, 43, 65, 67, 45]
 random.shuffle(numbers)
 numbers
[23, 43, 65, 45, 12, 67]

```
