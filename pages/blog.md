---
layout: misc
title: "Blog posts"
---

{% for post in site.categories.science %}
## [{{ post.title }}]({{ post.url }})

*by **{{ post.author | default: "xgrau" }}**, {{ post.date | date: "%-d %B %Y" }}*

{{ post.excerpt }}

****

{% endfor %}
