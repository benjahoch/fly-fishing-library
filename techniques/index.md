---
layout: default
title: Techniques
---

# Techniques

Casting styles, presentation methods, and tactical approaches for different water types and situations.

{% assign technique_pages = site.techniques | sort: 'title' %}
{% for item in technique_pages %}
- [{{ item.title }}]({{ item.url | relative_url }}){% if item.description %} — {{ item.description }}{% endif %}
{% endfor %}
