---
layout: default
title: Home
---

<main class="page-shell">
  <section class="hero">
    <img class="hero__photo" src="{{ site.logo | relative_url }}" alt="{{ site.title }}">
    <h1 class="hero__name">{{ site.title }}</h1>
    <p class="hero__description">{{ site.description }}</p>
    {% if site.linkedin_url or site.github_url or site.cv_url %}
      <nav class="hero__links" aria-label="Social links">
        {% if site.linkedin_url %}
          <a class="hero__link-pill" href="{{ site.linkedin_url }}" target="_blank" rel="noreferrer" aria-label="LinkedIn">
            <span class="hero__link-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" role="img" focusable="false">
                <path d="M6.94 8.5H3.56V20h3.38V8.5Zm.22-3.56C7.16 3.87 6.3 3 5.25 3S3.34 3.87 3.34 4.94c0 1.05.84 1.91 1.89 1.91 1.07 0 1.93-.86 1.93-1.91ZM20.66 13c0-3.47-1.85-5.08-4.31-5.08-1.99 0-2.88 1.09-3.37 1.86V8.5H9.6c.05.85 0 11.5 0 11.5h3.38v-6.42c0-.34.02-.68.12-.92.27-.68.88-1.39 1.91-1.39 1.35 0 1.89 1.05 1.89 2.58V20h3.38v-7Z"/>
              </svg>
            </span>
          </a>
        {% endif %}
        {% if site.github_url %}
          <a class="hero__link-pill" href="{{ site.github_url }}" target="_blank" rel="noreferrer" aria-label="GitHub">
            <span class="hero__link-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" role="img" focusable="false">
                <path d="M12 .5C5.65.5.5 5.65.5 12a11.5 11.5 0 0 0 7.86 10.92c.58.11.79-.25.79-.56v-1.97c-3.2.7-3.88-1.35-3.88-1.35-.52-1.33-1.28-1.68-1.28-1.68-1.04-.71.08-.7.08-.7 1.15.08 1.75 1.18 1.75 1.18 1.02 1.75 2.67 1.24 3.32.95.1-.74.4-1.24.72-1.53-2.55-.29-5.23-1.27-5.23-5.67 0-1.25.45-2.27 1.18-3.08-.12-.29-.51-1.46.11-3.04 0 0 .96-.31 3.15 1.18a10.9 10.9 0 0 1 5.74 0c2.18-1.49 3.14-1.18 3.14-1.18.63 1.58.24 2.75.12 3.04.74.81 1.18 1.83 1.18 3.08 0 4.41-2.69 5.37-5.25 5.66.41.35.77 1.04.77 2.11v3.13c0 .31.21.67.8.56A11.5 11.5 0 0 0 23.5 12C23.5 5.65 18.35.5 12 .5Z"/>
              </svg>
            </span>
          </a>
        {% endif %}
        {% if site.cv_url %}
          <a class="hero__link-pill" href="{{ site.cv_url | relative_url }}" aria-label="CV">
            <span class="hero__link-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" role="img" focusable="false">
                <path d="M7 2.75A2.25 2.25 0 0 0 4.75 5v14A2.25 2.25 0 0 0 7 21.25h10A2.25 2.25 0 0 0 19.25 19V8.56a2.25 2.25 0 0 0-.66-1.59l-3.31-3.31A2.25 2.25 0 0 0 13.69 3H7Zm6.25 1.9 3.1 3.1h-2.6a.5.5 0 0 1-.5-.5v-2.6ZM8 11.25c0-.41.34-.75.75-.75h6.5a.75.75 0 0 1 0 1.5h-6.5A.75.75 0 0 1 8 11.25Zm0 3.5c0-.41.34-.75.75-.75h6.5a.75.75 0 0 1 0 1.5h-6.5A.75.75 0 0 1 8 14.75Zm0 3.5c0-.41.34-.75.75-.75h4a.75.75 0 0 1 0 1.5h-4A.75.75 0 0 1 8 18.25Z"/>
              </svg>
            </span>
          </a>
        {% endif %}
      </nav>
    {% endif %}
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
