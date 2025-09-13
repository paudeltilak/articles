---
layout: default
title: My Articles Archive
---

# 🗂 My Articles Archive

Welcome! Below are links to all my articles:

<ul>
  {% assign pages_list = site.pages | sort: "path" %}
  {% for page in pages_list %}
    {% if page.path contains ".md" and page.path != "index.md" %}
      <li><a href="{{ page.url }}">{{ page.path }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
