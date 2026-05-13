---
layout: default
title: Blog
permalink: /blog/
---

<section class="page-header">
  <h1>Blog</h1>
  <p class="lede">按时间倒序，共 {{ site.posts | size }} 篇。</p>
</section>

<div class="archive">
  {% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
  {% for year_group in posts_by_year %}
    <h2 class="archive-year">{{ year_group.name }}</h2>
    {% for post in year_group.items %}
      <div class="archive-item">
        <span class="archive-date">{{ post.date | date: "%m-%d" }}</span>
        <span class="archive-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></span>
      </div>
    {% endfor %}
  {% endfor %}
</div>
