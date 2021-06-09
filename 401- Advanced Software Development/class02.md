# Testing

"A unit test is a specific type of code written to execrise the input, the output and the behavior of your code."[Gomes, 2017](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932).

Test driven development (TDD) is a strategy that involves alot of thinking before any code is written. In the exapmle given in this reading we see where there are various APIS which can be used to check gender based on name, however, the importnat aspects of the unit teasting comes in where data needs to be colleted, before the code is exectued or asserted in assuming that Max for example is really a male and not a female.

## Testing Cycle

The cycle of testing code in the TDD cycle is basically made up of three steps:

1. Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)

2. Write the feature and make the test pass! (you can dance after that)

3. Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)

Testing reduces bugs in your code and reduces the amount of fixes and refactorin you have to do before and or during deployment.

## Always Remember

* The greatest advantage about TDD is to craft the software design first

* Your code will be more reliable: after a change you can run your tests and be in peace

* Beginning may be hard — and that’s fine. You just need to practice!

## Recursion

**What is Recursion?**
The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily.

For example *f(n)*= 1+2+3+.....+n this fucntion mathematically is just adding by one to the value of *n*. Anopther way of approaching this is:

*f(n)* = 1              n=1

**f(n) = n + f(n-1)    n>1*

In the expression above f() is being added or called inside the fucntion, this is what recursion is.

I found this [Video](https://www.youtube.com/watch?v=wMNrSM5RFMc) which also helps to break down a recurssion.

Refrences:

[Gomes 2017](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)

[Recurssion](https://www.geeksforgeeks.org/recursion/)

[Video on Recursion](https://www.youtube.com/watch?v=wMNrSM5RFMc)
