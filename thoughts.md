---
layout: page
title: Thoughts
permalink: /thoughts/
---

<div class="home">

  {% if site.posts.size > 0 %}
    <div class="post-list">
      {% for post in site.posts %}
        <a class="post-link-container" href="{{ post.url | relative_url }}">
          {% assign date_format = site.minima.date_format | default: "%-d %B %Y" %}
          <span class="post-thumbnail-image"></span>
          <span class="h3">
            {{ post.title | escape }}
          </span>
          <span class="post-meta">{{ post.date | date: date_format }}</span>
          {% if post.subtitle %}
            <span> {{ post.subtitle | escape }}</span>
          {% endif %}
        </a>
      {% endfor %}
    </div>

    <!-- <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p> -->

  {% endif %}

</div>
