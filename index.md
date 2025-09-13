---
layout: default
title: My Articles Archive
---

# 🗂 My Articles Archive

Welcome! Below are links to all my articles:

{% assign sorted_static_files = site.static_files | sort: "path" %}

<ul>
  {% for file in sorted_static_files %}
    {% if file.path contains '.md' %}
      <li><a href="{{ file.path | relative_url }}">{{ file.path }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
