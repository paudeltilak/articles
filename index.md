---
layout: default
title: My Articles Archive
---

# 🗂 My Articles Archive

Welcome! Below are links to all my articles:

{% assign file_list = site.static_files | where: "extname", ".md" %}

<ul>
  {% for file in file_list %}
    {% if file.path != "/index.md" %}
      <li><a href="{{ file.path }}">{{ file.path }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
