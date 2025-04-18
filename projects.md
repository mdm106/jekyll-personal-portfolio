---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects-list">
  {% for project in site.projects %}
    <article class="project-article">
      <h6 class="project-title">{{ project.title }}</h6>
      {% if project.image %}
        <img src="{{ project.image }}" alt="{{ project.image_alt }}" class="project-image">
      {% endif %}
      <p class="main-text project-skills"><strong>{{ project.skills }}</strong></p>
      <p class="main-text project-text">{{ project.paragraph_1 }}</p>
      {% if project.paragraph_2 %}
       <p>{{ project.paragraph_2 }}</p>
      {% endif %}
      {% if project.github_link || project.app_link %}
        <div class="project-links">
            {% if project.github_link %}
                <a href="{{ project.github_link }}">
                    <i class="fab fa-github fa-2x"></i>
                </a>
            {% endif %}
            {% if project.app_link %}
                <a href="{{ project.app_link }}">
                    <i class="fa-solid fa-link fa-2x"></i>
                </a>
            {% endif %}
        </div>
      {% endif %}
    </article>
  {% endfor %}
</div>
