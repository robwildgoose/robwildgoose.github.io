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
<section class="experience-company row">
  <div class="col-12">
    <div class="section-heading">
      <h2>PureGym</h2>
    </div>
    {% assign puregym_roles = site.experience | where: "company", "PureGym" | sort: "order" %}
    <div class="timeline">
      {% for item in puregym_roles %}
        <div class="timeline-item">
          <div class="timeline-marker{% if item.period contains 'Present' %} timeline-marker-active{% endif %}"></div>
          <div class="timeline-card">
            <div class="timeline-top">
              <div>
                <h3>{{ item.role }}</h3>
              </div>
              <span class="status-badge">{{ item.period }}</span>
            </div>

            {% if item.summary %}
              <p class="timeline-summary">{{ item.summary }}</p>
            {% endif %}

            {% if item.tech %}
              <div class="tech-list">
                {% for tech in item.tech %}
                  <span class="tech-tag">{{ tech }}</span>
                {% endfor %}
              </div>
            {% endif %}
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</section>

<section class="experience-company row">
  <div class="col-12">
    <div class="section-heading">
      <h2>Next</h2>
    </div>
    {% assign next_roles = site.experience | where: "company", "Next" | sort: "order" %}
    <div class="timeline">
      {% for item in next_roles %}
        <div class="timeline-item">
          <div class="timeline-marker{% if item.period contains 'Present' %} timeline-marker-active{% endif %}"></div>
          <div class="timeline-card">
            <div class="timeline-top">
              <div>
                <h3>{{ item.role }}</h3>
              </div>
              <span class="status-badge">{{ item.period }}</span>
            </div>

            {% if item.summary %}
              <p class="timeline-summary">{{ item.summary }}</p>
            {% endif %}

            {% if item.tech %}
              <div class="tech-list">
                {% for tech in item.tech %}
                  <span class="tech-tag">{{ tech }}</span>
                {% endfor %}
              </div>
            {% endif %}
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</section>

<hr class="section-divider">
<section class="hero row">
  <div class="col-12">
  <h1 class="hero-role">App Projects</h1>
    <p class="lead-description">Personal apps and side projects.</p>
  </div>
</section>

<section class="projects-section row">
  <div class="col-12">
    <div class="section-heading">
      <h2>In Progress</h2>
    </div>
  </div>
  {% assign sorted_projects = site.projects | sort: "order" %}
  {% for project in sorted_projects %}
    {% if project.status == "In Progress" %}
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
    {% endif %}
  {% endfor %}
</section>

<hr class="section-divider">

<section class="projects-section row">
  <div class="col-12">
    <div class="section-heading">
      <h2>Retired</h2>
    </div>
  </div>
  {% assign sorted_projects = site.projects | sort: "order" %}
  {% for project in sorted_projects %}
    {% if project.status == "Now Retired" %}
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
    {% endif %}
  {% endfor %}
</section>