---
layout: page
hidden_title: "Blog"
title: ""
permalink: /blog/
---

<!-- <h1 class="custom-title">Blog Posts</h1> -->
<div class="custom-subtitle">Blog Posts</div>

<div class="posts">
  {% for post in site.posts %}
  <article class="post">
    <h2 class="post-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>

    <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date">
      {{ post.date | date_to_string }}
    </time>

    {% if post.description %}
    <p class="post-description">{{ post.description }}</p>
    {% endif %}
  </article>
  {% endfor %}
</div> 