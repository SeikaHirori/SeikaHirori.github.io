{% comment %}

<ul>
    {% for item in site.data.pinned %} 
        {% comment %}
        <li>
            <a href="{{ item.page_link }}">
                {{ item.name }}
            </a>
        </li>
        <br>
        {% endcomment %}


    
    {% endfor %}
</ul>
{% endcomment %}

{% for item in site.data.pinned %} 
    {% assign page_link = item.page_link %}
    {% assign name = item.name %}

- [{{name}}]({{page_link}})

    
{% endfor %}