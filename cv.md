---
layout: page
title: CV
description: Dr Ben Coombs — data scientist, analyst, and team lead.
permalink: /cv/
extra_css:
  - https://cdn.knightlab.com/libs/timeline3/latest/css/timeline.css
---

<div class="cv-layout">

  <div class="cv-intro">
    <p>A Chemist by training (PhD, Durham 2009), with 15+ years at the intersection of science, data, and engineering. Currently focused on data leadership — building teams, shaping data governance, and delivering high-value analytical outputs across research, manufacturing, and consultancy.</p>
  </div>

  <div class="cv-section">
    <span class="cv-section-title">Career Timeline</span>
    <div id="timeline-embed"></div>
    <script src="https://cdn.knightlab.com/libs/timeline3/latest/js/timeline.js"></script>
    <script>
      new TL.Timeline('timeline-embed', '/assets/timeline.json', {
        timenav_position: 'bottom',
        duration: 500,
        zoom_sequence: [0.5, 1, 2, 3],
        language: 'en'
      });
    </script>
  </div>

  <div class="cv-section">
    <span class="cv-section-title">Skills</span>
    <div class="skills-grid">
      <div class="skill-group">
        <h4>Languages</h4>
        <div class="skill-tags">
          <span class="tag">Python</span>
          <span class="tag">SQL</span>
          <span class="tag">R</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Data &amp; ML</h4>
        <div class="skill-tags">
          <span class="tag">pandas</span>
          <span class="tag">scikit-learn</span>
          <span class="tag">statsmodels</span>
          <span class="tag">PyTorch</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Visualisation</h4>
        <div class="skill-tags">
          <span class="tag tag-teal">Plotly</span>
          <span class="tag tag-teal">Tableau</span>
          <span class="tag tag-teal">Quarto</span>
          <span class="tag tag-teal">Matplotlib</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Notebooks</h4>
        <div class="skill-tags">
          <span class="tag tag-teal">Jupyter</span>
          <span class="tag tag-teal">Marimo</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Infrastructure</h4>
        <div class="skill-tags">
          <span class="tag tag-gray">Git</span>
          <span class="tag tag-gray">Docker</span>
          <span class="tag tag-gray">Azure</span>
          <span class="tag tag-gray">Databricks</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Leadership</h4>
        <div class="skill-tags">
          <span class="tag tag-gray">Team building</span>
          <span class="tag tag-gray">Data governance</span>
          <span class="tag tag-gray">Stakeholder mgmt</span>
        </div>
      </div>
    </div>
  </div>

  <div class="cv-download">
    <a href="{{ '/assets/CV_DrBenCoombs.pdf' | relative_url }}" class="btn btn-outline" download>⬇ Download CV (PDF)</a>
  </div>

</div>
