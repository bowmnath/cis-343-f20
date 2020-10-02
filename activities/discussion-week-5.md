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

*Note:* many of these are repeated from last week.
If we already covered one of these in your section,
we will skip it this week.

Given the parse tree below for an unknown grammar, which happens first,
the addition or the multiplication?
How do you know?
```
    <expression>
    /    |      \
  <id>   =      <expression>
   |            /     |     \
   A          <id>    +     <expression>
               |           /      |      \
               B          (  <expression> )
                            /     |      \
                         <id>     *      <id>
                          |                |
                          C                D
```

Give one possible set of grammar rules that could have generated the tree
above.
Is your grammar ambiguous?
If so, find an example to demonstrate.

What is the problem with having two parse trees for the same sentence?

Use the regular expression format
[from the slides](https://github.com/bowmnath/cis-343-f20/blob/master/slides/lexical-analysis.pdf).

Give a few examples of strings that match the following regular expression:
```
[Gg]ra+ce [Hopper]*
```

Give a few examples of strings that match the following regular expression:
```
\$.. is an (even | odd) number
```

Give a few examples of strings that match the following regular expression:
```
H[^aeiou]?
```

Give a few examples of strings that match the following regular expression:
```
.+[^s]$
```

For the problems that ask you to write a regular expression based on examples,
note that there are infinitely many possibilities.
Once you think you have it down,
try to come up with the simplest ones you can think of.

Write a regular expression that matches all of the following:
```
jlkhooaaee
prtwqa
bb
vctiaia
```

Write a regular expression that matches all of the following:
```
ssSsssssS
sssSssS
ssssS
ssS
```

Write a regular expression that matches all of the following:
```
7n8y9p
   <-- blank string
6e2c
8a8a8a8a8a8a8a
1m3y5p1a
```

Here is an example grammar based on Lisp
(actually, based on on a
[Wikipedia example](https://en.wikipedia.org/wiki/Programming_language#Syntax)
that was based on Lisp):
```
<expression> -> <atom>
<expression> -> <list>
<atom> -> <number>
<atom> -> <symbol>
<number> -> <digit><number>
<number> -> <digit>
<digit> -> 0
<digit> -> 1
...
<digit> -> 9
<symbol> -> <letter><symbol>
<symbol> -> <letter>
<letter> -> a
<letter> -> b
...
<letter> -> z
<list> -> '(' expression_list ')'
<expression_list> -> <expression><expression_list>
<expression_list> -> <expression>
<expression_list> -> " " (blank space)
```
Rewrite this using the variant of EBNF covered in the lectures.
The variant added `( A | B )` for OR,
`[]` for optional parts,
and `{}` for parts that are repeated 0 or more times.

Using your EBNF form or the original form
(it should make no difference),
write a few non-trivial sentences is the language.
It's up to you what non-trivial means.

Create parse trees for your example sentences.

# Note about regexs

We typically use regexs to search for a match within a larger string.
The full string
```
abcd12345
```
does not match the regular expression
```
[1-9]+
```
But, it does have a substring that matches.
Regular expressions will match the longest substring possible,
so a search would return
```
12345
```
even though `123`, `2`, etc., are also matches.
