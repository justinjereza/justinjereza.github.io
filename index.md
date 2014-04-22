---
layout: midnight
title: Blog without a name.
---

- [Foreman](foreman.html)
- [FreeNAS](freenas.html)

{% for post in site.posts %}
#### [{{ post.title }}]({{ post.url }}) | {{ post.date | date_to_string }}
{{ post.excerpt }}
{% endfor %}
