---
---

{% for page in site.pages %}
{% if page.name != "README.md" %}- [{{ page.name }}]({{ page.url }}){% endif %}
{% endfor %}

{% for page in site.pages | where: "name", "README.md" %}
{{ page.content | markdownify }}
{% endfor %}
