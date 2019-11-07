---
layout: misc
title: "Blog posts"
---

{% for post in site.categories.science %}
## [{{ post.title }}]({{ post.url }})

by {% if page.author %} {{ page.author }} {% else %} {{ site.author }} {% endif %}, {{ post.date | date: "%-d %B %Y" }} {% endfor %}

{{ post.excerpt }}

****

{% endfor %}
