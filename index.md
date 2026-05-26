---
layout: home
title: The DIY Chronicles
---

{% assign latest_post = site.posts.first %}

<article class="post">
  <header class="post-header">
    <h1 class="post-title">{{ latest_post.title | escape }}</h1>
    <p class="post-meta">{{ latest_post.date | date: "%b %-d, %Y" }}</p>
  </header>

  <div class="post-content">
    {{ latest_post.content }}
  </div>
</article>

<h2>Older Posts</h2>
<ul>
  {% for post in site.posts offset:1 %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
    </li>
  {% endfor %}
</ul>
