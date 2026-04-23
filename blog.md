---
layout: page
title: Blog
description: Writing on data science, team leadership, and analytics.
permalink: /blog/
---

<div class="post-list">
{% for post in site.posts %}
<article class="post-list-item">
  <div class="post-list-date">{{ post.date | date: "%d %b %Y" }}</div>
  <div>
    <h2 class="post-list-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-list-excerpt">{{ post.excerpt | strip_html | truncate: 180 }}</p>
    <div class="post-list-tags">
      {% for cat in post.categories %}<span class="tag tag-gray">{{ cat }}</span>{% endfor %}
    </div>
  </div>
</article>
{% endfor %}
</div>
