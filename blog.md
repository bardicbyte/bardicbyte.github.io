---
layout: blog
title: Blog
permalink: /blog/
---

<div class="blog-header">
  <h1>Blog Posts</h1>
  <p>Here I share my learnings and insights from various courses and projects, particularly focusing on my journey through the Fast AI course and software engineering best practices.</p>
</div>

<div class="blog-posts">
  {% for post in site.posts %}
    <article class="blog-post-card">
      <div class="post-meta">
        <span class="post-date">{{ post.date | date: "%B %-d, %Y" }}</span>
        {% if post.categories %}
          <div class="post-categories">
            {% for category in post.categories %}
              <span class="category-tag">{{ category }}</span>
            {% endfor %}
          </div>
        {% endif %}
      </div>
      <h2 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <div class="post-excerpt">
        {{ post.excerpt | strip_html | truncatewords: 50 }}
      </div>
      <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
    </article>
  {% endfor %}
</div> 