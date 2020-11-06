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

Note: the first few questions are repeats from last week.
We will skip those if we have already gone through them in your section.

1. What is the problem with the following?
```c
int* allocate() {
    int x = 0;
    return &x;
}

int main() {
    int* x = allocate();
    // use x
}
```

2. What are the lifetimes of `a` and `b` in the code below?
```c
void fun() {
    static int a;
    int b;
    // ...
}

int main() {
    fun();
    // ...
}
```

3. What are the scopes of `a` and `b` in the code above?

4. Describe what happens in the following code assuming
* static scoping, or
* dynamic scoping
```c
int x = 8;

void fun(int y) {
    int x = 9;
    fun2(y);
}

void fun2(int y) {
    int z = x + y;
}

fun()
fun2()
```

5. Recall the ternary operator discussed in lecture:
```c
v = a.val < b.val ? x : y
```
This is equivalent to an `if/else` statement.
Is it overall a net positive or net negative for a language to have such a
statement.
(It doesn't matter what you answer --
just be sure to back it up.)

6. Does the following code have any side effects?
```c
int a = 0;
int foo(int x) {
    int b = a + x;
    return b;
}
```

7. Used as part of a larger program,
would the function `foo` be referentially transparent?
Why or why not?

8. Does the following code have any side effects?
```c
int bar(int x) {
    static int a = 0;
    a = 2*x;
    return a;
}
```

9. Used as part of a larger program,
would the function `bar` be referentially transparent?
Why or why not?

10. If the code above is referentially transparent,
make some change so that it is not.
Otherwise, make the code referentially transparent.
It is fine if your modification changes the semantics of the function.

11. For each of the following,
decide whether it is a good use of operator overloading or not.
* Adding two Students gives their combined height
* Adding two GroceryItems gives their combined price
* Multiplying a vector and a scalar stretches or shrinks the vector by the
scalar
* Adding two Currency objects from different countries produces their
equivalent sum in US dollars

12. What type of runtime error will the following code produce?
```
float f = 5.6
for (int i = 0; < 100; i++) {
    f = f/10;
}
```

13. Which of the following would you expect to be *widening* conversions?
* float -> double
* long -> double
* long -> int
* int -> float
