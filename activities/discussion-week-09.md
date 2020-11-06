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

1. Java Classes do not meet the strictest definition of an ADT because they
allow `public` attributes.
* Why does this not match the definition of an ADT?
* What are some of the tradeoffs involved in the decision of whether to have
public variables?
* Would you prefer to see public variables removed from Java?

2. Give an example where inheritance is helpful.
It can be a hypothetical project or one that you have worked on in the past.

3. Python tuples are like lists,
except a tuple cannot be changed.
If we have tuple
```
a = ([1, 2], 3, 4)
```
and we try
```
a[0] = 0
```
Python will raise an error.
However, the following will work just fine:
```
a[0].append(1)
```
What is going on here?
This is one of those cases where it may be helpful to think at a lower level,
such as in terms of pointers or memory accesses.

4. To add more fun to the previous example,
the following code is a valid way to append two lists in Python:
```
[0, 1] + [2, 3]  #  == [0, 1, 2, 3]
```
So, based on the last append we tried, you would think
```
a[0] += [1]
```
would work.
It does not.
Any ideas why?
Your previous answer may give you a clue.

5. As discussed in lecture,
some languages prefix variables with clues as to the variables' types.
For example, we know the Perl variable `$name` is a scalar of some kind.
Consider your favorite language.
Would you support adding naming rules like the following?
* integer variable names must start with `i`
* floating-point variable names must start with `f`
* and so on

Why or why not?

6. Consider the C code below.
How do `x` and `p` differ in terms of address, value, and type?
```c
int main() {
    int x;
    int *p;

    x = 5;
    p = malloc(sizeof(int));
    *p = 5;
}
```

7. Examine the C code below.
```c
void s_incr() {
    static int stat = 0;
    stat += 1;
    printf("static stat: %d\n", stat);
}

void incr() {
    int stat = 0;
    stat += 1;
    printf("normal stat: %d\n", stat);
}

int main() {
    for (int i = 0; i < 5; i++) { incr(); }
    for (int i = 0; i < 5; i++) { s_incr(); }
}
```
The output is
```
normal stat: 1
normal stat: 1
normal stat: 1
normal stat: 1
normal stat: 1
static stat: 1
static stat: 2
static stat: 3
static stat: 4
static stat: 5
```
Can you explain what is happening here?

8. For each of the variables `a` - `d`,
is the variable allocated statically or dynamically?
Where is the variable stored? (Stack, heap, or global)
```c
int a;
int main() {
    static int b;
    int c;
    int *d;
    d = malloc(sizeof(int)*3);
}
```

9. When are each of the variables above deallocated?

10. What is the problem with the following?
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

11. What are the lifetimes of `a` and `b` in the code below?
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

12. What are the scopes of `a` and `b` in the code above?

13. Describe what happens in the following code assuming
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
