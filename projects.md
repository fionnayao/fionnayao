---
layout: page
title: Projects
permalink: /projects/
---

<div>
  {% if site.projects.size > 0 %}
    <ul class="post-list">
        {% for post in site.projects %}
        <li>
            <h3>
                <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
            </h3>
        </li>
        {% endfor %}
    </ul>
  {% endif %}

</div>