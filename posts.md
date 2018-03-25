---
layout: page
title: Posts
permalink: /posts/
---

<div class="home">

  {% if site.posts.size > 0 %}
  <h2 class="post-list-heading">{{ page.list_title | default: "..." }}</h2>
    <div class="post-list">
      {% for post in site.posts %}
        <a class="post-link-container" href="{{ post.url | relative_url }}">
          {% assign date_format = site.minima.date_format | default: "%-d %B %Y" %}
          <span class="post-meta">{{ post.date | date: date_format }}</span>
          <h4>
            {{ post.title | escape }}
          </h4>
          <span> {{ post.subtitle | escape }}</span>
          <div class="post-thumbnail-image"></div>
        </a>
      {% endfor %}
    </div>

    <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>
  {% endif %}

</div>
