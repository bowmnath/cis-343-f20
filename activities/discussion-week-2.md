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

* Is it possible to create an infinite loop by failing to use include guards?
    * If so, demonstrate. If not, why not?

* Is there an issue with the following code?
```
#include <stdlib.h>
int* newpointer(int* oldpointer) {
    int *b;
    b = oldpointer;
    return b;
}

int main(int argc, char** argv) {
    int *a, *b;

    a = malloc(sizeof(int)*10);
    b = newpointer(a);

    free(a);
    free(b);

    return 0;
}
```

* Is there an issue with the following code?
```
#include <stdlib.h>
int* newpointer(int* oldpointer) {
    int *b;
    b = oldpointer;
    return b;
}

int main(int argc, char** argv) {
    int *a, *b;

    a = malloc(sizeof(int)*10);
    b = newpointer(a);

    free(b);

    return 0;
}
```

* Name one feature of C that improves writability but hurts readability.

* Name one feature of C that improves writability but hurts reliability.

* Are there any features of C that you would bring into Java given the choice?

* Explain how the idea of a `void` function in C is not orthogonal.
(We may have mentioned this last week.)
Why might it still be useful?
Do you think it is worth the tradeoff?

# Coding

* Write a C program to reverse a string.
Note that C strings are arrays of characters **that end in the NUL character**.
The NUL character,
not to be confused with NULL,
is `'\0'`.
Try writing it two ways:
    * with a `for` loop. You will find the `strlen` function useful
    * with a `while` loop. The easiest way is still with the `strlen` function,
    but see if you can do it without that.
    Remember, strings end in `'\0'`
You should always compile your C wode with `-Wall` to enable warnings.
If you see a warning,
it is probably going to lead to an error when you run.

You may use the following code to read in the arguments to help you get
started.

```
#include <string.h>
#include <stdio.h>
#include <stdlib.h>


char* reverse_string(char *original) {
    // create this method using a for or a while loop
}


int main(int argc, char* argv[]) {

    // Normally we do *a lot* more error checking, but for now let's
    // keep it simple

    // The first argument is always the command itself.
    // The second argument is a string (char*)

    char *original = argv[1];
    char *reverse = reverse_string(original);

    // print the string and clean up

    return 0;
}
```
