{% for item in site.data.pinned %} 
    {% assign page_link = item.page_link %}
    {% assign name = item.name %}

- [{{name}}]({{page_link}})

{% endfor %}