{% assign sorted_repo = site.github.public_repositories   
    | sort: "pushed_at" 
    | reverse
%}

{% for repo in sorted_repo %}
{% assign is_it_blacklisted = false %}

{% for item in site.data.github_repo_blacklist %}
{% if item.repo_id  == repo.id %}
    {% assign is_it_blacklisted = true %}
    {% break %}
{% endif %}
{% endfor %}

{% if is_it_blacklisted == true %}

{% else %}

[{{ repo.name }}]({{ repo.html_url }}), ID: {{ repo.id }}

Last Updated: {{ repo.pushed_at | date_to_string }}

Languages: {{ repo.language }}   
<br>

{% endif %}


{% endfor %}