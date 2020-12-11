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

1. Describe, at a high level, the difference between a declarative language
and an imperiative language.

2. Which of the following are valid names for constants in Prolog?

```
Rabbit
w3nt
to
The
st_ore
```

3. Of the ones above that are not valid constant names, why not?

4. What would be a sensible way to give Prolog the fact that Messi is a soccer
player?

5. What would be a sensible way to tell Prolog that the Hulk is taller than
Thor?

6. How could you express the following idea in Prolog?
If one person is taller than another,
and the other person is taller than some third,
then the first person is also taller than the third?

7. How could you express the following set of facts and relationships in
Prolog?

All dogs are animals.
All cats are animals.
Golden retrievers are dogs.
Poodles are dogs.
Huskies are dogs.
Abyssinians are cats.
Manx are cats.

8. Given the above, how would you query whether Manx are animals?

9. How would you determine all dog breeds in the database?

10. Given the above, what would Prolog say if you asked whether a terrier was
a dog?

11. Complete the following (replace the `...`) so that `area` is a function to
return the area of any box in the database.

```prolog
width(box1, 10).
width(box2, 15).
height(box1, 5).
height(box2, 2).
area(A, B) :- width(A, Wide), height(A, Tall), ... .
```

12. The `area` "function" isn't really a function -- it is a rule.
We can do more with it than just query the area of a particular box.
What are the outputs of all of the following?

```prolog
?- area(box1, X).
?- area(X, 30).
?- area(X, Y).
?- area(box1, 100).
```
