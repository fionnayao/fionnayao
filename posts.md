---
layout: page
title: Posts
permalink: /posts/
---

<div class="home">

  {% if site.posts.size > 0 %}
  <h2 class="post-list-heading">{{ page.list_title | default: "..." }}</h2>
    <ul class="post-list">
      {% for post in site.posts %}
        <li>
          {% assign date_format = site.minima.date_format | default: "%-d %B %Y" %}
          <span class="post-meta">{{ post.date | date: date_format }}</span>

          <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
          </h3>
        </li>
      {% endfor %}
    </ul>

    <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>
  {% endif %}

</div>