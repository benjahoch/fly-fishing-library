---
layout: default
title: Index
---

# 🎣 Fly Fishing Library

A personal knowledge base for fly fishing — organized field notes, species profiles, technique breakdowns, hatch charts, regional water guides, and gear notes. Maintained with Claude.

---

<div class="index-grid">
  <a class="index-card" href="{{ '/species/' | relative_url }}">
    <span class="card-emoji">🐟</span>
    <div class="card-title">Species</div>
    <div class="card-count">{{ site.species | size }} entries</div>
  </a>
  <a class="index-card" href="{{ '/techniques/' | relative_url }}">
    <span class="card-emoji">🪝</span>
    <div class="card-title">Techniques</div>
    <div class="card-count">{{ site.techniques | size }} entries</div>
  </a>
  <a class="index-card" href="{{ '/hatches/' | relative_url }}">
    <span class="card-emoji">🦋</span>
    <div class="card-title">Hatches</div>
    <div class="card-count">{{ site.hatches | size }} entries</div>
  </a>
  <a class="index-card" href="{{ '/regions/' | relative_url }}">
    <span class="card-emoji">🗺️</span>
    <div class="card-title">Regions</div>
    <div class="card-count">{{ site.regions | size }} entries</div>
  </a>
  <a class="index-card" href="{{ '/gear/' | relative_url }}">
    <span class="card-emoji">🎒</span>
    <div class="card-title">Gear</div>
    <div class="card-count">{{ site.gear | size }} entries</div>
  </a>
</div>

---

## Recently Updated

<ul>
{% assign all_docs = site.species | concat: site.techniques | concat: site.hatches | concat: site.regions | concat: site.gear %}
{% assign sorted_docs = all_docs | sort: 'last_updated' | reverse %}
{% for doc in sorted_docs limit:8 %}
  <li><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a> <small>— {{ doc.last_updated }}</small></li>
{% endfor %}
</ul>
