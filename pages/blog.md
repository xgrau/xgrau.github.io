---
layout: misc
title: "Blog posts"
---

{% for post in site.posts %}

**[{{ post.title }}]({{ post.url }})**, {{ site.data.settings.post_date_prefix }} {% assign d = page.date | date: "%-d"  %} {{ page.date | date: "%B" }} {% case d %} {% when '1' or '21' or '31' %}{{ d }}st {% when '2' or '22' %}{{ d }}nd {% when '3' or '23' %}{{ d }}rd  {% else %}{{ d }}th{% endcase %}, {{ page.date | date: "%Y" }} by {% if page.author %} {{ page.author }} {% else %} {{ site.author }}  {% endif %}


{{ post.date | date: "%-d %B %Y" }} 

> {{ post.excerpt }}

&nbsp;

{% endfor %}
