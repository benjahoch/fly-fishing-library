---
layout: default
title: Species
---

# Species

Profiles for warmwater and coldwater species — behavior, habitat, feeding patterns, and the flies that work.

{% assign species_pages = site.species | sort: 'title' %}
{% for item in species_pages %}
- [{{ item.title }}]({{ item.url | relative_url }}){% if item.description %} — {{ item.description }}{% endif %}
{% endfor %}
