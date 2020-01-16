---
layout: misc
title: "Blog posts"
---

{% for post in site.posts %}

**[{{ post.title }}]({{ post.url }})**, {{ post.date | date: "%-d %B %Y" }} 

> {{ post.excerpt }}

{% endfor %}
