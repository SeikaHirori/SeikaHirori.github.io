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

            {% assign folder_categories = {{ post.categories | join: "_" | replace: "_", " " }} %}
            {% if folder_categories %}
                <h5> Category: {{ folder_categories }}</h5>
            {% endif %}

            <p>{{ post.excerpt | strip_html | truncatewords:75 }}</p>

        </li>
        <br>
    {% endfor %}
</ul>