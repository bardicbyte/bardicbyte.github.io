---
layout: default
title: Blog
permalink: /blog/
---

<header class="header">
  <h1>Blog Posts</h1>
  <nav class="nav-links">
    <a href="/">Home</a>
    <a href="/#about">About</a>
    <a href="/#education">Education</a>
    <a href="/#experience">Experience</a>
    <a href="/#projects">Projects</a>
  </nav>
</header>

<div class="card">
  <p>Here I share my learnings and insights from various courses and projects, particularly focusing on my journey through the Fast AI course.</p>
</div>

<div class="post-list">
  {% for post in site.posts %}
    <article class="post-item">
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h2 class="post-title">
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <div class="post-excerpt">
        {{ post.excerpt }}
      </div>
    </article>
  {% endfor %}
</div> 