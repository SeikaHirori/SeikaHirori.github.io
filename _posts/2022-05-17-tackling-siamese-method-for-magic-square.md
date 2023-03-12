---
layout: post
title: Tackling Siamese Method for Magic Square
date: '2022-08-19T11:53:00.005-07:00'
repo: 
project_id: 
tags:
- Imported

---

[[Exercise: Part 4 of \"Programming exercise: Magic square (4
parts)]{.underline}](https://java-programming.mooc.fi/part-12/4-multidimensional-data)

**[Abstract]{.underline}**:

A "while" loop is used for implementing the Siamese method algorithm.
For the loop, "continue" was not used at any point as it will cause an
infinite loop. Various "if" statements were used to ensure that the
program is following the rules of the Siamese method. The most difficult
part to figure out was Lines 36 - 38, as it was difficult to figure out
when to move downwards if both the "X" and "Y" coordinates are out of
bounds.

---

**[Detailed Version]{.underline}**:

The fourth part of the exercise was interesting as it wanted to
implement the [[Siamese method
algorithm]{.underline}](https://en.wikipedia.org/wiki/Siamese_method).
The first 3 parts did not take too long to solve, but the fourth part
took about 6-8 hours to solve. The amount of approachable options were
vast, BUT that large amount makes it difficult to figure out "okay,
where do I go from here?". It was like a tree branch OR trying to
navigate through a complex maze. For the context of creating a Magic
Square, it is 5x5 or there are a total of 25 numbers.

Before starting, the parameter (named "size") to make the Magic Square
has to be an odd number that is greater than or equal to 3. If the
conditions were not met, the program should immediately end.

First off, variable "x" would be assigned as the "column" and variable
"y" would be the "row". According to the Siamese method, the first
number will always have to be on the first row and in the middle column.
"y" will start off with the number "0" for the first row as we are going
through an index/element. For "x", the middle column was calculated by
using the formula "size / 2". This would be returned as an integer,
which is perfect for this context as the outcome of a quotient would
always be rounded down. This would always ensure that "y" would start in
the middle as the number is being plugged into an index/element.

Immediately afterwards, the second step was creating two variables, the
first one being "value" and was assigned as "1" as this was the starting
number. The second variable was "totalValues", where it was the product
of "size \* size". Then, a "while" loop was used, and it would only end
once "value" is bigger than "totalValues". "value" would increase right
before the loop restarts.

Several conditions and actions were created as seen in the code. Once
the current loop goes through all of the conditions to the point that
the value inside the index/element "0", the "x" and "y" are used to
place the current "value" into the respective index before starting the
loop again.

There were several hurdles when it came to solving the code.

I initially tried to use a "for" loop and using "continue" if any of the
conditions were met, but this did not work out as I intended. As a
result, I swapped over to using a "while" loop as I did not want the
value amount to increase regardless of the status. I tried to use
"continue" as I thought it would be beneficial to start the loop over if
any of the conditions were met AND check the conditions, but this
resulted in an infinite loop. It would be forever stuck at the first
condition and continuously modifying ONLY that one variable. This would
apply whenever "continue" was used. It took a while to realize that
"continue" was not going to work out for this situation, so I scrapped
using "continue".

The next difficult thing was handling whenever "x" or "y" went out of
bounds. Initially, I had it that if either conditions were met, their
values would reset to their respective spot (according to Siamese
method). Seeing this, I broke the two apart into their own conditions
and resets.

The last thing that was extremely difficult was figuring out the
situation (when at value 16) regarding these two things:

1.  If moving diagonally would result in both "x" and "y" being out of
    > bounds.

2.  The space below was available (value in element was "0").

I thought that the condition on Line 49 would deal with this potential
situation, but it did not. I experimented with trying to use "continue",
but it created an infinite loop as a result. It took a long time to
experiment and figure out the solution, but the conclusion was
eventually reached. The code would have to be nested under the first
condition on Line 33. The reason is that without this nested code, the
"checkY" and "checkX" would reset "x" and "y" after they were moved
diagonally. This would not move downwards of said situation. Then, there
were three conditions to move "downwards":

1)  The space below MUST be available (value below must be "0")

2)  "checkX" returns true, meaning "x" is out of bounds.

3)  "checkY" returns true, meaning "y" is also out of bounds.

After experimenting with various sizes of the Magic Square, this
condition proved to be viable.

Minor things:

-   Should most/all checks return the boolean as "true" or "false\'\' as
    > the default option?

-   Attempting to condense some actions within some boolean methods, but
    > that made it hard to track down what was happening.

    -   Eventually decided to move the "action" codes into their own
        > respective methods.

-   A thing I did not realize until later on was that the exercise
    > provided code (in the class "MagicSquare.java") when it came to
    > reading and placing values within the arrays. I wrote my code to
    > handle it until I replaced it with the methods from the mentioned
    > class.

How could I improve my code?

-   The naming schemes for methods as I was unsure how to name them at
    > the time.

-   For the "if" conditions on Line 36, it could be condensed into its
    > own method.

The takeaways:

-   Having used multidimensional data from this chapter, I think it is
    > possible to NOW create the Tic Tac Toe program.

-   Implementing an algorithm within a multidimensional data.

-   With how long it took to resolve part 4:

    -   I am grateful that I learned and have been using Git and GitHub
        > to save the many revisions. I thought the files were hidden
        > too deep for MacOS's terminal to reach, but I found a
        > workaround for Git to work. It has saved me so much time
        > throughout the Java Programming II section.

    -   After completing MOOC.fi's Java Programming course, Test-Drive
        > Development is the next step in my learning journey to
        > increase my personal workflow. I think this might suit my
        > nature of "how can I break this and how far can I push the
        > boundaries" approach that I utilize when I play video games. A
        > [[course]{.underline} is provided by [MOOC.fi
        > here]{.underline}](https://tdd.mooc.fi/).

-   Regardless of how "simple" the implementation might seem, it's still
    > best practice to execute the action of a code one at a time. When
    > it comes to refactoring, THEN that's when it is okay to see if it
    > is possible to mesh some of the actions together. If anything,
    > create a separate new method AND then combine the actions under
    > said separate new method.

This part of the exercise was interesting, so I thought about sharing my
experience about it!
