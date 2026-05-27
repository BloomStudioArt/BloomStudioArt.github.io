---
layout: default
title: About
---

<section class="about-page">
  <div class="about-header">
    <h1>About</h1>
    <p>Bloom Studio is an interactive art initiative exploring the
    intersection of sound, light, and participation. We create experiences
    that invite audiences to become part of the work itself.</p>
  </div>

  <div class="about-team">
    <h2>Team</h2>
    <div class="team-grid">
      {% assign members = site.members | sort: "order" %}
      {% for member in members %}
        {% include member-card.html member=member %}
      {% endfor %}
    </div>
  </div>

  <div class="about-contact">
    <a href="mailto:{{ site.email }}">{{ site.email }}</a>
    <a href="https://github.com/BloomStudioArt" target="_blank" class="github-link"
    >
      GitHub
    </a>
  </div>
</section>