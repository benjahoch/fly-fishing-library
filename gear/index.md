---
layout: default
title: Gear
---

# Gear

Rod builds, reel setups, line selection, fly boxes, and equipment notes.

{% assign gear_pages = site.gear | sort: 'title' %}
{% for item in gear_pages %}
- [{{ item.title }}]({{ item.url | relative_url }}){% if item.description %} — {{ item.description }}{% endif %}
{% endfor %}
