---
---

{% for page in site.pages %}
{% if page.name != "README.md" and page.name != "index.md" %}
  - [{{ page.name }}]({{site.baseurl}}/{{ page.url }})
{% endif %}
{% endfor %}

{{ site.pages | where:"name","README.md" }}
