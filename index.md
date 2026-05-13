---
layout: default
title: 首页
---

<section class="intro">
  <h1>你好，我是许晓斌 / Xu Xiaobin</h1>
  <p class="lede">在 <a href="https://github.com/juven">GitHub</a> 上写代码，业余记录读书、旅行、技术想法。</p>
  <p>联系：<a href="mailto:juvenshun@gmail.com">juvenshun@gmail.com</a></p>
</section>

<section class="recent-posts">
  <h2>最近的博文</h2>
  <div class="post-list-compact">
    {% for post in site.posts limit:5 %}
      <article class="post-list-item">
        <span class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        {% if post.excerpt %}<p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 180 }}</p>{% endif %}
      </article>
    {% endfor %}
  </div>
  <p class="archive-link"><a href="{{ '/blog/' | relative_url }}">查看所有博文 →</a></p>
</section>
