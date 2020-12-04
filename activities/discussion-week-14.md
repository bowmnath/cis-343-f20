In your groups, answer the following questions.
No need to report the answers to me --
this is just for practice.

I will be dropping in and out of rooms to facilitate to the discussions and in
case you have any questions.
Think of it like me walking around the classroom and listening to different
groups.
Again, this isn't meant to be for a grade,
so don't be concerned about giving a wrong answer even if I am in the room.
You can also flag me down in Zoom if you have a question even if I'm not in the
room
(I think the button in Zoom looks like a question mark).

# Questions

1. Describe, at a high level, the purpose of the function `mystery`.

```scheme
(define (mystery a b)
  (mystery-helper a b 0))

(define (mystery-helper a b c)
  (if (> a b)
    c
    (mystery-helper (+ a 1) b (+ a c))))
```

2. How could you fill in the code below so that the final result is a list
containing each element of `x` divided by the corresponding element of `y`?

```scheme
(define x (list 1 2 3))
(define y (list 4 5 6))
(map (lambda [fill in here]) x y)
```

3. Fill in the code below so that the final result is 120
(the product of 4, 5, and 6).
Note that a simple `*` will not work here.

```scheme
([fill in here] (list 4 5 6))
```

4. Python's `map` function returns a `map` object instead of a list.
What is the difference, and why is the `map` object beneficial?

5. According to the slides,
a subprogram "may or may not have a name."
How could a subprogram without a name be useful?

6. In C, function signatures may look like the following:
```c
int add_nums(int a, int b);
float divide_nums(float a, float b);
```

In JavaScript, function signatures always begin with the `function` keyword,
such as:
```javascript
function add_nums(a, b){ }
function divide_nums(a, b){ }
```

In terms of readability, writability, and reliability,
what are the tradeoffs of these different ways of declaring functions?

7. Some languages allow functions to accept a variable number of arguments.
Give an example of a function for which this might be helpful.
Is there any downside?

8. Briefly describe the difference between formal parameters and actual
parameters.

9. Describe the similarities and differences between pass-by-value and
pass-by-result.

10. For each of the following,
state whether it is used for in-mode, out-mode, or in-out mode passing.
    * Pass-by-value
    * Pass-by-result
    * Pass-by-value-result
    * Pass-by-reference

11. If a large array is passed to a function,
which will be more efficient:
pass-by-value or pass-by-reference.

12. What is the result of the following code if the language uses shallow
binding? Deep binding?

```python
def fun1():
    x = 10

    def fun2(some_fun):
        x = 5
        some_fun()

    def fun3():
        print(x)

    fun2(fun3)
```

13. Assume a programming language did not keep track of closures
(referencing environments of functions declared within functions).
What would go wrong with the following?

```python
def print_greeting(salutation):
    def personal_greeting(name):
        print("%s %s!" % (salutation, name))
    return personal_greeting

hello = print_greeting("Hello")
hi = print_greeting("Hi")
hello("Section 1")
hi("Section 2")
```
