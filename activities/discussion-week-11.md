The questions will be posted as homework.
However, for this assignment specifically,
you are allowed to work in pairs or small groups.

# Questions

Everyone knows that grading is done via random number generation.
The trick is figuring out the correct distribution to use.
You are going to write code that simulates grades for various types of
coursework.

1. First, try to make an easy assignment as follows.
Write a function (`grade1`) that:
* generates a random number between 88 and 95
* assigns a letter grade according to a simple scale with no +/- grading
(A is 90 or above, B is 80 - 89, etc.)

You will want to use the `random` function.
When passed one argument `x`,
the function `random` returns a random integer in the half-open range `[0, x)`.

2. Next, you get grumpy because you are thinking of how Game of Thrones ended.
Make an extremely hard exam with scores between 8 and 30.
Assign letter grades as before.
However, you should write your function in such a way that your grading logic
could be reused even if the score distribution changed
(i.e., as a helper function).
Call the function `grade2`.

3. To make your grading process more efficient in the future,
you need to make your program more flexible.
Make a function that can create your future grading functions.

Create a single function (`grade3`) that
* takes two arguments, the high and low grades for the assignment
* returns a function that accepts no arguments and outputs letter grades
for random scores between the low and high grades (inclusive)

Test it out on a few ranges.
Remember -- you are not directly generating a grade here.
You are returning a function that generates grades.

4. Write a function to evaluate the expression
```
a + (b % c)*5*d - 5*d**(b % c)
```
where `**` denotes exponentiation (`expt` in Scheme).
Notice that `(b % c)` and `5*d` both appear twice in the expression.
Write your function so that the values are computed just once.
(Hint: remember `let`)
