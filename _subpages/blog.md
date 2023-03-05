---
layout: default
title: Blog
---

# {{ page.title }}

<ul>
    {% for post in site.posts %}
        <li>
            <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
            {{ post.date | date_to_string }}
            {{ post.excerpt }}
        </li>
    {% endfor %}
</ul>