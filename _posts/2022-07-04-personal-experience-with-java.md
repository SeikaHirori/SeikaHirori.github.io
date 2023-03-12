---
layout: post
title: Personal Experience with Java Programming (MOOC.fi)
date: '2022-08-19T12:05:00.001-07:00'
repo: 
project_id: 
tags:
- Imported

---


TL;DR:

The Java Programming (MOOC.fi) course is great for beginners who started
their self-taught programming journey! There were some hiccups, but that
did not deter my progress through the course. The experience was an
incredible kick off to my self-taught programming journey.

**How did I find** MOOC.fi and its Java Programming course? It was free
course commonly mentioned on r/LearnProgramming and r/LearnJava. I
initially started with the [[Python Programming MOOC
2022]{.underline}](https://programming-22.mooc.fi/) course but I swapped
over to the [[Java Programming
MOOC]{.underline}](https://java-programming.mooc.fi/) course early on.
The primary reason I swapped was because an apprenticeship opportunity
required Java knowledge, and a friend suggested switching over from the
Python Java for said opportunity.

**For my progression** through the course, it was not too bad! Trying to
understand the basic foundations of programming was difficult... BUT
once I understood how they functioned, I felt unstoppable at learning
ANYTHING :3. The grade check was helpful to see which scenario I did not
account for in my code! I utilized Google, Stack Overflow, and
documentation to dig into information I need help understanding.
However, I completed up until Part 14.2 as I did not need to utilize the
whole toolset from JavaFX.

**Why do I like this** over other introduction courses? For me, I learn
best by being hands-on first. Fortunately, this course synergies well
with my learning style. I loved how it taught learners how to use the
tools in the intro section, and then they explained how those tools work
on a deeper level in the advanced section. For example, [[part
12]{.underline}](https://java-programming.mooc.fi/part-12) explains how
type parameters, ArrayLists, and Hashmaps function on a deeper level.
They introduced [[Unit Testing via
JUnit]{.underline}](https://java-programming.mooc.fi/part-6/3-introduction-to-testing)
AND briefly mentioned TDD (Test-Driven Development). They also
introduced platforms/ frameworks like JavaFX. As a result, you get to
fiddle around with graphs, photos, audio, and build a game!

**There were small hiccups** along my journey through the course. Some
Finnish-to-English translation was lost, so some wording and grammatical
structure might not make sense. The lack of opportunities to practice
unit testing outside the introduction in Part 6. This is likely the
grade check function, as writing test code would conflict with the TMC
plugin AND pre-made tests from the course. It was a struggle trying to
implement JUnit as the grade check exists. It also made TDD impossible.
You could set up a separate workspace to do this, but that would cost
extra time to copy and paste code back and forth. The style-check could
be better distinguished like how it's done in [[CS50x's style
check]{.underline}](https://cs50.readthedocs.io/style50/).

The course doesn't account for users on non-x86 devices (I'm assuming it
was published before Apple Silicon devices were widely released). In
order to find the instructions, you have to really go out of your way to
find information on how to set up an IDE and Java packages. Here's a
link to setup VSCode that works for Apple Silicon devices on MacOS,
[[https://www.mooc.fi/en/installation/vscode/]{.underline}](https://www.mooc.fi/en/installation/vscode/).

**Would I recommend the Java course?** YES FOR BEGINNERS!... But that's
an elephant in the room from earlier: the [[Python Programming MOOC
2022]{.underline}](https://programming-22.mooc.fi/) course.

I progressed up until Part 3.2 before I swapped over to the [[Java
Programming MOOC]{.underline}](https://java-programming.mooc.fi/)
course. It looks like the Python course is the main introductory course
for University of Helsinki's Computer Science department now. It's being
updated yearly on MOOC.fi from my observation.

If you want to IMMEDIATELY jump into learning programming, I recommend
going with the Python version as the IDE setup is FAR simpler. This
rings especially true if you are using MacOS with Apple Silicon. Setup
was easier with Python than having to manually setup Java for VSCode. If
you attempt to run the provided IDE (Netbeans or Eclipse) through
Rosetta, the performance will be a hindrance. It will freeze after
testing. It is possible to install the TMC (TestMyCode) plug-in
extension separately with a newer build of either NetBeans or Eclipse,
but it will require more time and research to set up. I found that
VSCode was easier to set up on Apple Silicon (aside from setting up
Maven). If you use Windows OR MacOS on an Intel-powered Apple device, I
think using the course's provided IDE setup should be less of a hassle
for both Python and Java courses.

If I were to start from scratch, I would still go with the Java course.
Before switching to the Java course, I went up to Part 3 of the Python
course. I STRUGGLED with the Python syntax since my eyes could not
comprehend reading code with the large amount of whitespace. With the
Java syntax, it gave me guidance to where a line/ body of code started
and stopped. It also ingrained in me to be mindful of the syntax (i.e.
"{ }", "( )"). Thanks to the Java syntax giving the understanding of
this, I do not struggle as much when reading Python's syntax now.

I'll mention it here: When you complete about 80% of the introduction or
advance section, you are [[awarded a
certificate]{.underline}](https://www.mooc.fi/en/profile/completions)
for the respective section! It's a nice moral boost to make you go "AWWW
YEAH I MADE PROGRESS AS A PROGRAMMER Y'ALL W00T W00T!"

**What is next for me?** I wanted to learn more about data structures
and algorithms, and my friend suggested that it was a great step to
tackle next. There were two free courses I found:
[[Algs4]{.underline}](https://algs4.cs.princeton.edu/home/) and
[[Pythonds3]{.underline}](https://runestone.academy/ns/books/published/pythonds3/index.html).

If you want to stick with Java as the main programming language,
[[Algs4]{.underline}](https://algs4.cs.princeton.edu/home/) is a great
option. However, you will need to set up their library manually if you
are on MacOS with Apple Silicon. Once you do, you will spend time
learning how to use their nonstandard library. This feels like a
traditional course... which makes sense since it is from Princeton
University. They provide the textbook and online course for free! Video
lectures accompany the lessons as well, which are found in the online
course. The links are:

\- [[Textbook]{.underline}](https://algs4.cs.princeton.edu/home/)

\- [[Course \| Part
1]{.underline}](https://www.coursera.org/learn/algorithms-part1)

\- [[Course \| Part
2]{.underline}](https://www.coursera.org/learn/algorithms-part2)

If you do not mind switching over to Python,
[[Pythonds3]{.underline}](https://runestone.academy/ns/books/published/pythonds3/index.html)
(from Runestone.academy) is another option. This is more reading (like
Java/Python MOOCfi), but video is provided throughout the course! They
do a great job explaining the Python syntax, so transitioning from Java
(and possibly C, C#, JavaScript, etc) would be less of a struggle.

I also wanted to learn about TDD as I think it suits my style of "here's
point A and point B; let's set up the staircase to make it possible".
MOOCfi does provide a [[TDD course]{.underline}](https://tdd.mooc.fi/).
However, the main language for its exercises is Javascript.

**What have I been doing** since I completed Java Programming MOOC?

-   I attempted to learn JavaScript on the fly for the TDD course, but
    > this proved to be unsuccessful for me. For me to understand
    > JavaScript, I think I would need to dedicate focused time to it.
    > Instead, I implemented the general idea/concepts for TDD for all
    > code I have been writing since...

-   I have been building personal projects on the side! I created a list
    > of project ideas that either would be fun, resolve my needs, or
    > encourage me to learn and refine tool sets. For my current
    > project, my objectives were to learn Python and implement TDD. I
    > have more opportunities to practice the Python syntax since...

-   I am currently going through Pythonds3! It's teaching Python in the
    > first chapter, and it has not been as difficult a transition as I
    > thought. I will provide my full thoughts after I finish the
    > course. My impression as of finishing Chapter 1, it has been
    > pretty great! I am excited to get into the meatier sections! Plus,
    > the exercises have been handy in understanding the lessons!

```{=html}
<!-- -->
```
-   Running alongside the course, I have been implementing TDD with
    > PyTest. It was confusing at first, but I am getting the grasp of
    > it ever so slowly. I am reading through the [[TDD
    > MOOC]{.underline}](https://tdd.mooc.fi/) as the materials are
    > applicable on a general level.

-   PyTest: THIS TOOL IS SO HANDY. That's all I need to say.

-   The documentation and resources for Python have been amazingly
    > plentiful. Oddly, I find it easier for me to comprehend than I did
    > with Java. Not sure why, but I'll take it.

-   I tried out Algs4 before Pythonds3, but I spent a lot of time
    > fighting to set up the library in my IDE. The struggles of using
    > MacOS with Apple Silicon :'(

I am still excited about this journey! I do hope that I will get to the
point where I can gain industry experience soon! In the meantime, I will
continue to learn all of these wonderful technologies.

***Courses mentioned (URLs):***

**Introduction courses:**

-   Java Programming (MOOC.fi)  --- 
    > [[https://java-programming.mooc.fi/]{.underline}](https://java-programming.mooc.fi/)

-   Python Programming (MOOC.fi)  --- 
    > [[https://programming-22.mooc.fi/]{.underline}](https://programming-22.mooc.fi/)

**Data structures and algorithms:**

-   Pythonds3 (Runestone.academy)  --- 
    > [[https://runestone.academy/ns/books/published/pythonds3/index.html]{.underline}](https://runestone.academy/ns/books/published/pythonds3/index.html)

-   Algs4 ( Princeton University \| Online textbook)  --- 
    > [[https://algs4.cs.princeton.edu/home/]{.underline}](https://algs4.cs.princeton.edu/home/)

-   Algs4 ( Princeton University \|Course \[Part 1 of 2\])  --- 
    > [[https://www.coursera.org/learn/algorithms-part1]{.underline}](https://www.coursera.org/learn/algorithms-part1)

**TDD (Test-Driven Development):**

-   TDD (MOOC.fi)  --- 
    > [[https://tdd.mooc.fi/]{.underline}](https://tdd.mooc.fi/)

**MISC:**

-   CS50x, a free introductory course to CompSci (Harvard University)
    >  --- 
    > [[https://cs50.harvard.edu/x/]{.underline}](https://cs50.harvard.edu/x/)
