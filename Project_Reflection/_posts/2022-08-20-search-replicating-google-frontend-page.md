---
layout: post
title: Search | Replicating Google Frontend Page
repo: 
project_id: 
tags:
    - CS50w
---

**Abstract**: Replicate Wikipedia by using Django, MarkDown2, and HTML
according to the specifications. Focused on creating views.py and other
things within the Django framework. For writing tests, it was a
self-imposed journey to figure out how to test Front-end by experting
with Selenium, Pylenium, and Playwright.

**Repo**:
[[https://github.com/WaToArt/replicate-wiki]{.underline}](https://github.com/WaToArt/replicate-wiki)

**Specifications**:
[[https://cs50.harvard.edu/web/2020/projects/1/wiki/]{.underline}](https://cs50.harvard.edu/web/2020/projects/1/wiki/)

\_\_\_

This is my first completed project that uses
[[Django]{.underline}](https://www.djangoproject.com/) as the web
framework. The focus of this project was learning how templates/views.py
worked within Django.

I will not lie: It was difficult understanding how Django worked. I had
to constantly refer to the CS50w's lectures and examples, Django's
official doc, StackOverFlow (SOF), and various other resources found via
Google. This is understandable as Django was new to me... but honestly,
understanding how to develop a website was so daunting compared to doing
various back-end stuff.

I think the biggest personal hindrance was misunderstanding how
variables are handled in Django. Another hurdle was forgetting a step
when setting up a new app and/or page. Lastly, various misc things were:

-   Enabling a global variable to be used in all Django templates

-   How to implement MarkDown2

-   How CS50w's module "util" worked

-   How "request.POST" and "request.GET" works

The biggest struggle of them all: Not knowing how to use the Test-Driven
Development (TDD) methodology during the process. I was not sure how to
test the Front-end at all. I went in blind developing the wiki project
to specs. After I finished building most of the project, I tried to dig
up info on how to test the front-end. Somewhere on Google search, I
learned that a form of testing for Front-end is called end-to-end
testing (according to
[[atlassian]{.underline}](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing);
this is called by various names too according to several different
posts).

Starting off on the journey to trying to test the front-end (with my
current knowledge of templates and views.py), I saw various
recommendations on reddit that mentioned [[Obey the Testing
Goat]{.underline}](https://www.obeythetestinggoat.com/) (OtTG). I
skimmed the first few chapters, and they recommended Selenium. This was
my first front-end test tool. I gave it a try, but I was unsatisfied by
the confusing terms and slow performance. Plus, the setup to run
Selenium within Python was hard. I found some solutions after various
Google searches, but the experience turned me off from it.

Then, I stumbled upon the TDD [[Django workshop
doc]{.underline}](https://test-driven-django-development.readthedocs.io/en/latest/index.html).
For this one, they only used [[Django's test
client]{.underline}](https://docs.djangoproject.com/en/4.1/topics/testing/tools/).
A great thing about using Django's test client was that the project
didn't need to run actively to work. However, it was difficult reading
through the official docs since they didn't provide examples of how each
function worked. When they do provide an example, they do not show what
library was imported. This becomes a duck hunt to figure out what they
imported. More notably, the test tool did not meet my needs of how a
user would interact with the website. For example, the interaction would
be:

1.  Start on the homepage.

2.  Locate and click on the link for creating a new page.

Afterwards, I found out about Pylenium. I saw it mentioned when I looked
up "Cypress Python" since Cypress was only supported on JavaScript.
Writing tests was seamless with Pylenium and the setup was not too hard.
HOWEVER, it seemed like the automated thing to download WebDrivers
seemed to not be working on my M1 Macbook Air. I ran it locally, but it
was a minor inconvenience. I thought I would settle on Pylenium but the
small scaleness of the tool/ project plus it looking like it depends on
Selenium-wire, which makes me wary.

As the last stop, I saw Playwright as another big tool that was
mentioned alongside Selenium and Cypress. It works on most major
programming languages like JavaScript, Python, .NET, and Java. I tried
out the examples from the docs, and wrote some Playwright tests for the
project. It is a bit confusing how locators and expects works, but the
documentation for these things are understandable. Despite the small
struggles, the experience has been quite lovely. It smoothly integrates
with Pytest too!

**Concluding**: First section of the project was focused on using Django
for the Wiki project was a difficult task. It will take a while to get
used to it, but learning it will be a great asset for myself. The second
half focused a lot more time trying to figure out how to test the
front-end, which will be crucial for implementing TDD going forward.

I wrote a lot more about learning the testing tools than the wiki
project itself. I think the struggle for the Wiki could be talked about
more, but I felt like it was more "ahhh HA!" moments like "Wait, how
does the Python code I wrote be used for the Django template variable?"
and "o how does request.GET and request.POST work?".

I think the more crucial part was discovering the front-end test tools.
It was nice to have built the Wiki project, but it was frustrating not
having automated tests whenever I broke the code. For myself, writing
tests afterwards feels... odd? It feels like I am forgetting many
situations to assert for.

Moving forward for WebDev (and Django), I will use the Django test
client and Playwright to test. Django's test client works when the
website isn't running, and I think it is great for setting foundational
tests like status codes, templates, and so on. Playwright will handle
the rest, such as

For plans now: I will pause going through CS50w for now and resume it
after I tackle Obey the Testing Goat (OtTG). The reason being: OtTG
tackles TDD with the emphasis on Django and using Front-end testing
tools. From quickly glancing at the book, it does not seem like too long
of a detour. Plus, the methodology seems like life-long-lasting compared
to just learning tools that will constantly change. Me learning how to
TDD for WebDev will be beneficial to me in my opinion.

Tools used:

-   [[Django]{.underline}](https://www.djangoproject.com/)

-   [[MarkDown2]{.underline}](https://github.com/trentm/python-markdown2)

-   [[Pytest]{.underline}](https://docs.pytest.org/en/7.1.x/)

-   [[Selenium]{.underline}](https://www.selenium.dev/)

-   [[Pylenium]{.underline}](https://docs.pylenium.io/)

-   [[Playwright]{.underline}](https://playwright.dev/)

Note to self for future test code:

-   Instead of writing the whole url (ex:
    > "[[https://localhost:8000/create]{.underline}](https://localhost:8000/create)"),
    > you can use fstring to fill in the base url link (in this case,
    > "[[https://localhost:8000]{.underline}](https://localhost:8000)")
    > as it can be more scalably.

LAST FEW OUTLINES:

-   Pylenium experience

    -   Found via searching "Cypress for Python/Django"

-   Playwright

    -   Found via reddit after finding comparsions between cypress and
        > selenium

    -   Can't use both Pylenium and Playwright at the same time due to
        > the files generated by Pylenium.

-   CONCLUSION:

    -   Took a LONG TIME to understand how Django templates worked.

    -   Dug into how front-end testing so I can TDD

    -   Will pause on CS50w for now to work through Obey the Testing
        > Goat. It doesn't seem too long.
