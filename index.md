---
layout: default
title: My Articles Archive
---

# 🗂 My Articles Archive

Welcome! Below are links to all my articles:

{% assign sorted_pages = site.pages | sort: "path" %}

<ul>
  {% for page in sorted_pages %}
    {% if page.path != "index.md" %}
      <li><a href="{{ page.url | relative_url }}">{{ page.path }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
