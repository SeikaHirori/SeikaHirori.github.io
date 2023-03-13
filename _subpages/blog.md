---
layout: default
title: Blog
---

# {{ page.title }}

<ul>
    {% for post in site.posts %}
        <li>
            <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
            <h3> {{ post.date | date_to_string }} </h3>
            {{ post.excerpt | strip_html | truncatewords:25 }}
        </li>
        <br>
    {% endfor %}
</ul>