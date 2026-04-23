---
layout: default
title: Blog
description: Notes and writing from James.
permalink: /blog/
---
<section class="blog-index-header">
  <p class="eyebrow">Writing</p>
  <h1>Blog</h1>
  <p class="hero-copy">
    Posts now live inside the main personal website repo instead of on a separate project.
  </p>
</section>

{% if site.posts.size > 0 %}
<section class="post-list">
  {% for post in site.posts %}
  <article class="post-card">
    <p class="post-card-date">{{ post.date | date: "%B %-d, %Y" }}</p>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
  </article>
  {% endfor %}
</section>
{% else %}
<section class="empty-state">
  <h2>No posts published yet.</h2>
  <p>New writing will show up here once posts are added to the repo.</p>
</section>
{% endif %}
