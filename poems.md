---
layout: default
title: 诗
permalink: /poems/
---

<section class="page-header">
  <h1>诗</h1>
  <p class="lede">许晓斌写的诗，共 {{ site.poems | size }} 首。</p>
</section>

<div class="poem-list">
  {% assign poems = site.poems | sort: "date" | reverse %}
  {% for poem in poems %}
    <article class="poem-list-item">
      <h3><a href="{{ poem.url | relative_url }}">{{ poem.title }}</a></h3>
      {% if poem.date %}
        <span class="poem-meta">{{ poem.date | date: "%Y-%m-%d" }}{% if poem.place %} · {{ poem.place }}{% endif %}</span>
      {% endif %}
    </article>
  {% endfor %}
</div>
