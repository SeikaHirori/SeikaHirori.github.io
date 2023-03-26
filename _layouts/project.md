---
layout: default
---

{% comment %}
<!-- Use plugin "GitHub metadata" to obtain list of repo items from  -->
{% endcomment %}

{% assign sorted_github_repo = site.github.public_repositories   
    | sort: "pushed_at" 
    | reverse
%}

{% comment %}
<!--- Reset all values to nil so it doesn't carry over to next loop --->
{% endcomment %}
{% assign url = nil %}
{% assign title = nil %}
{% assign repo_link = nil %}
{% assign repo_id = nil %}
{% assign created_date = nil %}
{% assign last_updated = nil %}
{% assign tech = nil %}
{% assign tags = nil  %}
{% assign short_summary = nil %}

{% comment %}
<!-- Grab information from GitHub data -->
{% endcomment %}
{% for entry in sorted_github_repo %}

{% endfor %}


{% assign title = page.title | default: site.default_empty %}
{% assign created_date = page.date | date_to_string  | default: site.default_empty%}

{% comment %}
<!-- Display the information -->
{% endcomment%}
<div>
    <h1> {{ title }} </h1>
    <h5>
        Original Date: <span class="info">{{ created_date }}</span>
    </h5>
    <h3>
        Last updated: <span class="info">{{ page.last_updated | date_to_string   | default: site.default_empty  }} </span>
    </h3>
    <h3>
        Tech: <span class="info">{{ page.tech | join: ", "  | default: site.default_empty  }}</span>
    </h3>
    <h4>
        Tags: <span class="info">{{ page.tags | join: ", "   | default: site.default_empty  }}</span>
    </h4>
    <h4>
        Repo: <a href="{{ page.repo_link }}">{{ page.repo_link   | default: site.default_empty  }}</a>
    </h4>
    <h4>Specifications: 
        {% if page.specifications %}
        <a href="{{ page.specifications }}">{{ page.specifications }}</a>
        {% else %}
            ໒(⊙ᴗ⊙)७✎▤
        {% endif %}
     </h4>
</div>
<hr>
<br>

<div>
    {% assign short_summary = page.short_summary | strip_newlines %}
    {% if short_summary == "" %}
        {% assign short_summary = "໒(⊙ᴗ⊙)७✎▤" %}
    {% endif %}

    <h2>Summary:</h2>
    <p>{{ short_summary }}</p>
</div>
<hr>
<br>

<div>
    <h2>Reflection Posts:</h2>

    {% assign posts = site.posts | where_exp: 'post', "post.project_id contains page.project_id" %}
    {% assign post_size = posts | size %}
    {% if post_size > 0 %}
    <ul>
        {% for post in posts %}
        <li>
            <a href="{{ post.url | relative_url }}">{{ post.date | date_to_string }}: {{ post.title }}</a>
        </li>
        {% endfor %}
    </ul>
    {% else %}
        <p>໒(⊙ᴗ⊙)७✎▤</p>
    {% endif %}
</div>


<div>
    
    {% assign content = content | strip_newlines %}
    {% if content == "" %}
    {% else %}
        <hr>
        <br>
        {{ content }}
    {% endif %}
</div>