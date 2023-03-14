---
layout: default
title: Projects
last_updated: 2023-03-14
---
<div>
    <h1> {{ page.title }}</h1>
    <h5>Last updated: {{ page.last_updated | date_to_string }}</h5>
    <p> My GitHub repository contains my all of my latest projects, which can be here: <a href="https://github.com/SeikaHirori">https://github.com/SeikaHirori</a>
    </p>
</div>
<br>

<div>
    <h2>Here are some highlights!</h2>
    {% include portfolio_showcase.html %}
</div>
<br>

<div>
<h2> Here are some other projects :3 </h2>
<ul>
    {% for project in site.projects %}
        {% assign is_in_showcase = false %}
        {% for showcase in site.data.portfolio_showcase %}
            {% if showcase.project_id == project.project_id %}
                {% assign is_in_showcase = true %}
                {% break %}
            {% endif %}
        {% endfor %}

        {% if is_in_showcase %}
            {% continue %}
        {% else %}
            <li>
                <h2><a href="{{project.url}}">{{project.title}}</a></h2>
                <h4> Tech: {{project.tools}}</h4>
                <p>
                    {% if project.short_summary %}
                        {{ project.short_summary}}
                    {% else %}
                        {{ project.excerpt }}
                    {% endif %}
                </p>
            </li>
        {% endif %}

        
    {% endfor %}
</ul>
</div>
<br>

<div>
    <h3>If you like to view more of my projects, they can be viewed <a href="https://github.com/SeikaHirori?tab=repositories">here.</a></h3>
</div>
