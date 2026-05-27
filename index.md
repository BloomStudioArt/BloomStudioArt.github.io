---
layout: default
title: Home
---

<section class="home-page">

  <div class="home-statement">
    <p>Bloom Studio is an interactive art initiative exploring the intersection of sound, light, and participation.</p>
    <a href="{{ '/gallery/' | relative_url }}" class="home-statement__link">View Work</a>
  </div>

  {% assign featured = site.projects | sort: "date" | reverse | first %}
  {% if featured %}
  <div class="home-featured">
    <span class="home-featured__label">Recent Work</span>
    <a href="{{ featured.url }}" class="home-featured__card">
      {% if featured.cover %}
      <div class="home-featured__image">
        <img src="{{ site.cloudinary }}{{ featured.cover }}" alt="{{ featured.title }}" />
      </div>
      {% endif %}
      <div class="home-featured__body">
        <h2>{{ featured.title }}</h2>
        <p>{{ featured.summary }}</p>
        {% if featured.tags %}
        <ul class="tags">
          {% for tag in featured.tags %}
          <li>{{ tag }}</li>
          {% endfor %}
        </ul>
        {% endif %}
      </div>
    </a>
  </div>
  {% endif %}

</section>