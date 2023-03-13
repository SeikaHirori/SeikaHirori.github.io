---
layout: post
title: Tic-Tac-Toe with JavaFX
repo: 
project_id: 
tags:
    - Imported
---




**Abstract**: Create the Tic-Tac-Toe game utilizing JavaFX as the
GUI/Front-end. Learn and implement 'event-based programming'. 

[Exercise: [[Tic-Tac-Toe (3
parts)]]()]

[- Thought process:]

[- I wanted to use multiple classes, but I was overwhelmed by the huge
amount of possible approaches. I knew that I wanted to use multiple past
concepts and ideas (i.e. multidimensional array), but I was not sure how
to incorporate it with JavaFX.]

[- It took a while to learn how to utilize 'event-based programming',
but it was very powerful when I learned how it worked.]

[- Most of the general components came down as I wrote it. Had I
realized these ideas earlier, they would have been separated into their
own classes. Since the ideas came towards the end of the project, it was
difficult to separate some of these ideas.]

[- Trying to break down the steps was hard. Looking at TMC\'s code, the
way they went about it makes sense.]

[- I wanted to refactor, but I didn\'t want to do so after looking at
TMC\'s code. If I did, my approach would be similar to TMC\'s.]

[- Future:]

[- If I were to rework this right now from scratch, the first thing is
to migrate basic code and functions into a logic class (i.e. turn order,
integrating int\[\]\[\]). I originally had done this BUT TMC didn't like
this code, but centering 'Turn:'. I had used HBox as it worked for my
needs.]

[- In the far future, I do want to approach this application whenever I
learn more concepts and use a different programming language and
tools.]

[- NOTEWORTHY: using '.isBlank' worked locally, but TMC didn\'t want
that. In order to maintain the consistent button size, the workaround
used both \'.replaceAll(\" \", \"\") and '.isEmpty' to achieve the same
results.]

[- Missing features:]

[- Return feedback to users on who won OR was a tie game.]

> [- Was unsure how to count up the tallies with only buttons, but using
> a multidimensional array would suffice.]
>
> [- Show a visual of which buttons gave the winner the victory.]
>
> [- Wanted to use array, but unsure how to incorporate it where it
> works together with the buttons in the application.]

[- No 'restart ' and 'quit/close' program function.]

> [- Option: once the game finishes, have the last button change to
> another subview with a prompt to start a new session.]
