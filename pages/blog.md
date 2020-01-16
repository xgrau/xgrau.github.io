---
layout: misc
title: "Blog posts"
---

{% for post in site.posts %}
* **[{{ post.title }}]({{ post.url }})**, by {% if page.author %} {{ page.author }} {% else %} {{ site.author }}{% endif %}, {{ post.date | date: "%-d %B %Y" }} 

> {{ post.excerpt }}

****

{% endfor %}
