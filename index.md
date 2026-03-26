---
layout: default
title: Home
---

<main class="page-shell">
  <section class="hero">
    <img class="hero__photo" src="{{ site.logo | relative_url }}" alt="{{ site.title }}">
    <h1 class="hero__name">{{ site.title }}</h1>
    <p class="hero__description">{{ site.description }}</p>
  </section>

  <section class="projects" aria-label="Projects">
    {% for project in site.projects %}
      <article class="project-card">
        <div class="project-card__media">
          {% if project.gif %}
            <img src="{{ project.gif | relative_url }}" alt="{{ project.title }}">
          {% else %}
            <div class="project-card__placeholder">
              Add a GIF path in <code>_config.yml</code> for this project to show a preview here.
            </div>
          {% endif %}
        </div>

        <div class="project-card__content">
          <h2 class="project-card__title">{{ project.title }}</h2>
          <p class="project-card__description">{{ project.description }}</p>

          {% if project.link_url %}
            <a class="project-card__link" href="{{ project.link_url }}" target="_blank" rel="noreferrer">
              {{ project.link_text | default: "View project" }}
            </a>
          {% endif %}
        </div>
      </article>
    {% endfor %}
  </section>
</main>
