---
layout: misc
title: "Blog posts"
---

{% for post in site.posts %}

## [{{ post.title }}]({{ post.url }})

*by **{{ post.author | default: "xgrau" }}**, {{ post.date | date: "%-d %B %Y" }}*

{{ post.excerpt }}

****

{% endfor %}
