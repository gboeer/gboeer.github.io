---
layout: default
title: Home
---

# Welcome to Legor's plAIground

Here are my recent posts:

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%B %d, %Y" }}
  {% if post.description %}<br><small>{{ post.description }}</small>{% endif %}
  {% if post.tags %}<br><small>Tags: {{ post.tags | join: ', ' }}</small>{% endif %}
{% endfor %}
