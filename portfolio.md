---
layout: page
title: Portfolio
description: Analysis projects, notebooks, and dashboards — a mix of tools and techniques from across data science.
permalink: /portfolio/
---

{% if site.projects.size > 0 %}
<div class="portfolio-grid">
{% for project in site.projects %}
<article class="card project-card">
  <div class="card-body">
    <div class="project-card-type">
      <span class="tag {% if project.type == 'notebook' or project.type == 'marimo' %}tag-teal{% elsif project.type == 'dashboard' %}tag{% else %}tag-gray{% endif %}">{{ project.type | default: 'project' }}</span>
    </div>
    <h2 class="project-card-title"><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
    <p class="project-card-desc">{{ project.description }}</p>
    <div class="project-card-links">
      {% if project.github %}<a href="{{ project.github }}" class="btn btn-outline btn-sm" target="_blank" rel="noopener">GitHub</a>{% endif %}
      {% if project.notebook %}<a href="{{ project.notebook }}" class="btn btn-primary btn-sm" target="_blank" rel="noopener">Notebook</a>{% endif %}
      {% if project.demo %}<a href="{{ project.demo }}" class="btn btn-primary btn-sm" target="_blank" rel="noopener">Demo</a>{% endif %}
    </div>
  </div>
</article>
{% endfor %}
</div>
{% else %}
<div class="portfolio-empty">
  <p>Projects coming soon.</p>
</div>
{% endif %}
