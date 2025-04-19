---
layout: page
title: Blog
permalink: /blog/
---

# Blog Posts

Here I share my learnings and insights from various courses and projects, particularly focusing on my journey through the Fast AI course.

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h2>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul> 