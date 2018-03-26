---
layout: projects
title: Projects
permalink: /projects/
---

{% if site.projects.size > 0 %}


  {% for post in site.projects %}

  <section data-project="{{ post.title | downcase }}">

    <a class="projects-link-container" href="{{ post.url | relative_url }}">
      <img class="projects-thumbnail-image" src="/assets/company/{{post.company_logo}}" alt="{{ post.company_logo }}" />
      <span> {{ post.description }}</span>
      <span class="projects-button-link" role="button"> View {{ post.title }}'s projects ↝ </span>
    </a>

  </section>

  {% endfor %}

{% endif %}