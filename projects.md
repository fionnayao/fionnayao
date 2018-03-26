---
layout: page
title: Projects
permalink: /projects/
---

<div>
  {% if site.projects.size > 0 %}

  <ul class="post-list">
    {% for post in site.projects %}

    <a class="post-link-container" href="{{ post.url | relative_url }}">
      <div class="post-thumbnail-image company-project-image">
        <img src="/assets/company/{{post.company_logo}}" alt="{{ post.company_logo }}" />
      </div>
      <p class="company-project-description">{{ post.description }}</p>
    </a>

    {% endfor %}
  </ul>

  {% endif %}
</div>
