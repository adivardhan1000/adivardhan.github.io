---
layout: inner
title: Blogs
permalink: /blogs/
---
{% for blog in site.blogs %}
<li>
    <a href="{{ blog.url }}">{{ blog.title }}</a> - {{ blog.date | date: "%B %d, %Y" }}
</li>
{% endfor %}
