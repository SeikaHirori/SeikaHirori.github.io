{% assign default_empty_value = site.default_empty %}
{% assign materials = site.data.learning_materials_beginner %}



{% for item in materials %}

    {% assign title = item.title  %}
    {% assign link = item.link %}
    {% assign format = item.format | capitalize | default: default_empty_value %}

    {% case item.is_it_free %}
        {% when true %}
            {% assign cost = 'YESH!' | default: default_empty_value %}
        {% when false %}
            {% assign cost = 'no :(' | default: default_empty_value %}
        {% else %}
            {% assign cost = default_empty_value %}
    {% endcase %}

    {% assign tech = item.tech | join: ", " | default: default_empty_value %}

    {% assign tag = item.tags | join: ", " | default: default_empty_value %}

    {% assign summary = item.summary | default: default_empty_value %}

{% if item.title %}

## * {{ title }}

<span class="headliner">Link</span>: {% if link %}
[{{ link | default: default_empty_value }}]({{ link }})
{% else %}
{{default_empty_value}}
{% endif %}

<span class="headliner">Format</span>: {{ format }}

<span class="headliner">Is it free?</span>: {{ cost }}

<span class="headliner">Tech</span>: {{ tech }}

<span class="headliner">Tags</span>: {{ tag }}

<span class="headliner">Summary</span>: {{ summary }}

<br>
{% endif %}

{% endfor %}