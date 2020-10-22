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

1. Under which of the following conditions do we know that a grammar is
ambiguous?
    * two derivations exist for the same sentence
    * a leftmost and a rightmost derivation exist for the same sentence
    * two parse trees exist for the same sentence

2. Prove that the following grammar is ambiguous
```
<start> -> <start><line>
         | <line>
<line> -> <start>
        | <id>
<id> -> (A|B|C)
```

3. Identify the lexemes in the following sentence and give their tokens:
```
The (very) sad moose ate 5 pies.
```
Justify your answer.

4. Give a few strings that match the following regular expression:
```
[Mm]ice (ea)+t [^c]ats*
```

5. Consider the following grammar:
```
<S> -> <I> <E> <I>
<E> -> (+|-|*|/)
<I> -> (a|b|c|d)
     | "("<I>")"
```
Is the following sentence valid in this grammar?
```
(a+b) + c
```

6. Convert the following BNF to EBNF:
```
L -> SaL
   | Sa
S -> z
   | y
   | Sy
```
Recall the variant of EBNF covered in the lectures.
The variant added `(A|B)` for OR,
`[]` for optional parts,
and `{}` for parts that are repeated 0 or more times.

7. Write a regular expression that matches all of
```
bbbbaaaaaa
bbbbba
bb
bbbaaaa
```
but does not match any of:
```
aa
ba
bab
```
Strive for simplicity in your expression.

8. Make a case for and against the inclusion of the `case` statement
(also called the `switch` statement) in a language.
Be sure to discuss in terms of readability, writability, and/or reliability.

9. C functions can return primitive types and `struct`s, but cannot return
arrays.
This is an example of a lack of ... in the language.

10. Should `b` be freed before the return statement?
Why or why not?
```
#include <stdlib.h>
int main(int argc, char** argv) {
    int *a, *b;

    a = malloc(sizeof(int)*10);
    b = a;
    a = malloc(sizeof(int)*5);

    free(a);

    return 0;
}
```

11. What is the issue with the following code?
```
void nextNum(int x) {
    return x + 1;
}

int main(int argc, char** argv) {
    int y;
    int x = 5;

    y = nextNum(x);

    return 0;
}
```

12. Writing an interpreter and running a program is one way to determine the
program's _____ (syntax or semantics?)

13. Give one upside and one downside to using static linking in C
(as opposed to dynamic linking)

14. Use the pairwise disjoint test to determine whether a top-down parser can
parse the following grammars:
```
Grammar 1:
A -> bA | Cd
C -> e | bd

Grammar 2:
A -> b | C
C -> e | dC
```
