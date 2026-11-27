---
layout: default
banner: "/assets/images/home-banner-image.jpg"
banner_alt: "Photo by Lukasz Szmigiel on Unsplash"
---

<section class="hero row">
  <div class="col-12">
    <h1 class="hero-role">Mobile App Developer</h1>
    <p class="lead-description">{{ site.description }}</p>
    <hr class="section-divider">
  </div>
</section>

<section class="hero row">
  <div class="col-12">
  <h1 class="hero-role">App Projects</h1>
    <p class="lead-description">Personal apps and side projects.</p>
  </div>
</section>

<section class="projects-section row">
  {% assign sorted_projects = site.projects | sort: "order" %}
  {% for project in sorted_projects %}
      <div class="col-12 col-md-6">
        <a href="{{ project.url | relative_url }}" class="project-card h-100">
          <div class="project-meta-top">
            {% if project.status %}
              <span class="status-badge status-{{ project.status | slugify }}">{{ project.status }}</span>
            {% endif %}
            {% for platform in project.platforms %}
              <span class="meta-tag">{{ platform }}</span>
            {% endfor %}
          </div>

          <h3>{{ project.title }}</h3>
          <p>{{ project.summary }}</p>

          {% if project.tech %}
            <div class="tech-list">
              {% for item in project.tech limit:3 %}
                <span class="tech-tag">{{ item }}</span>
              {% endfor %}
            </div>
          {% endif %}
        </a>
      </div>
  {% endfor %}
</section>