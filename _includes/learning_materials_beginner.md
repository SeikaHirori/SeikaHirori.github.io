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


{% assign summary = item.summary | default: default_empty_value %}

{% if item.title %}

## * {{ title }}

Link: {% if link %}
[{{ link | default: default_empty_value }}]({{ link }})
{% else %}
{{default_empty_value}}
{% endif %}

Format: {{ format }}

Is it free?: {{ cost }}

Summary: {{ summary }}

<br>
{% endif %}

{% endfor %}