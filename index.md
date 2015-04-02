---
---

{% for page in site.pages %}
{% if page.name != "README.md" %}
  - [{{ page.name }}]({{site.baseurl}}/{{ page.url }})
{% endif %}
{% endfor %}

{{ site.pages | where:"name","README.md" }}
