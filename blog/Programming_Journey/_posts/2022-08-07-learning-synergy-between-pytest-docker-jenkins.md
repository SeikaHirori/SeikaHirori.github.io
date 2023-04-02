---
layout: post
title: 'Learning: The synergy between Pytest, Docker, and Jenkins'
repo: 
repo_id:
- 518595990 
tags:
- Imported
---

**Abstract**: Learned the utility of Docker and Jenkins, and how to combine
them with pytest to automate testing for personal repos. Resources used/
mentioned are listed in the "documentation" folder in the repo. This is
a shorter one, but it will improve my workflow.

I saw Docker and Jenkins in passing, and these tech intrigued me in how
they worked. The push was when I went to test my code from an old
project on a separate PC, but it didn't run. I wanted to REALLY make
sure that all future code had a reduced chance of suffering the "but it
worked on my computer uwu".

I tried to dive head on to see how Jenkins functioned first. The thought
of automating tests was intriguing, but I was not how it worked. I found
from a post that Jenkins could be used to automate pytest for a GitHub
repo. That became my key end goal.

I saw that Docker was used in that toolset, but the method they
mentioned was VASTLY different compared to the instructions provided by
the official Jenkins site. For a bit, I followed Jenkins\'s instructions
to set up the Docker instructions. The Jenkin's guide was fine for what
I needed to do, but I learned about how Docker worked from the
[[MOOC.FI]{.underline}](https://devopswithdocker.com/) as I wanted to
understand what was happening. After learning Docker from the course, I
resumed setting up Jenkins. I installed the majority of Jenkin's
instructions, but I forgot about the Docker DIND section.

Following the Jenkin's Docker page, I set up the Dockerfile for Jenkins.
Afterwards, I followed the post to set up a Dockerfile for Python.
Although optional, I set up Docker Compose to run Jenkins as it would
remove the need to run some commands.

Once I launched Jenkins and followed the setup instructions. This part
was not too bad. Credentials wise, it took a while to figure out how it
worked. Following a youtube video, I was able to set up Jenkins to a
repo. I followed the blog to set up the automated testing. I struggled
to understand what the code did, but eventually figured out that it was
automating the commands (in Shell) I would use to set up Docker.

A downside was that in order for tests to run after each update to
GitHub, but a public link to Jenkins was needed. For my needs, this
method was not feasible. The next best alternative was to run tests at
designated times.

To conclude, setting all of this stuff is pretty confusing AND there is
room for error at various points. I think it was completely unnecessary
to learn for my current stage of learning programming as well. However,
these tools are powerful when implemented. Also, this exercise practice
provides a great foundation/template for future reference to
containerize and test projects with Docker. In the end, I am glad that I
learned about Docker and Jenkins to be implemented with my current
workflow. In the future, Jenkins will be deployed on a separate device
to auto the tests.
