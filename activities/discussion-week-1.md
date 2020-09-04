Give the pros and cons of each of these using the ideas from our book.
Overall, do you think each one is a net good or net bad?
    * `for` loops.
    These are not strictly necessary.
    Anything you can do with a `for` loop,
    you can do with a `while` loop.
    * Ruby does not require parentheses when making subroutine calls.
    All of the following are valid:
    ```ruby
    fun1(fun2(arg1))
    fun1(fun2 arg1 )
    fun1 fun2 arg1
    ```
    * Many languages have two types of comments: block and single-line.
    For example, using `//` vs `/* */` in Java.
    * Inclusion of the `char` (character) data type.
    Some languages, such as Python, have only strings.
    * C allows `void` functions,
    which are functions that do not return anything,
    but does not have a `void` type.
    ```c
    void add(int* x) {  // fine to do
        *x = *x + 1;
    }

    int num;
    void val;  // will not compile
    ```
    * In Java, primitive data types and objects are treated differently under
    assignment.
    ```
    int x = 5;  // x is a value
    House y = new House();  // y is a reference
    ```

**Stop here for now.**
We'll do the second set in another breakout.

Imagine everyone agreed to design a single new programming language and use
it for all domains.
Give arguments for and against this "one language to rule them all".
Overall, do you think it would be a good idea or not?

Personal preference: do you prefer langauges that end blocks with
* right braces?
* if/fi do/od?
* whitespace?
Next, analyze the pros and cons with ideas from this class.
