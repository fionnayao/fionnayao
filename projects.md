---
layout: projects
title: Projects
permalink: /projects/
---

{% if site.projects.size > 0 %}

  {% assign sorted_projects = site.projects | sort:'order' %}
  {% for post in sorted_projects  %}

  <section data-project="{{ post.title | downcase }}">

    <div class="portfolio-background" style="background-image:url(/assets/company/{{post.project_logo}})"></div>

    <a class="projects-link-container" href="{{ post.url | relative_url }}">
      <img src="/assets/company/{{post.company_logo}}" alt="{{ post.company_logo }}" />
      <p>{{ post.description }}</p>
      <span class="projects-button-link" role="button"> See my&nbsp;work for {{ post.title }}&nbsp;↝ </span>
    </a>

  </section>

  {% endfor %}

{% endif %}