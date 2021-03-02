---
layout: page
title: alumni
permalink: /alumni/
description: Our current alumni list.
nav: true
social: true  # includes social icons at the bottom of the page
---

## Alumna

---

{% assign team = site.data.team %}

<!-- Alumna Projects Grid -->
<div class="projects grid">
  {% for alumna in team %}
  {% if alumna.section.alumna %}
  <div class="grid-item">
    {% if alumna.externalWebpage %}
    <a href="{{ alumna.externalWebpage }}" target="_blank">
    {% elsif alumna.webpage %}
    <a href="{{ alumna.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if alumna.img %}
        <img src="{{ alumna.img | relative_url }}" alt="alumna thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ alumna.firstName | append: " " | append: alumna.lastName }}</h5>
          <p class="card-text">{{ alumna.titles.default }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if alumna.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ alumna.github }}" target="_blank">
                <i class="fab fa-github gh-icon"></i>
                </a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if alumna.externalWebpage %}
    </a>
    {% elsif alumna.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Alumnus

---

<!-- Alumnus Projects Grid -->
<div class="projects grid">
  {% for alumnus in team %}
  {% if alumnus.section.alumnus %}
  <div class="grid-item">
    {% if alumnus.externalWebpage %}
    <a href="{{ alumnus.externalWebpage }}" target="_blank">
    {% elsif alumnus.webpage %}
    <a href="{{ alumnus.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if alumnus.img %}
        <img src="{{ alumnus.img | relative_url }}" alt="alumnus thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ alumnus.firstName | append: " " | append: alumnus.lastName }}</h5>
          <p class="card-text">{{ alumnus.titles.default }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if alumnus.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ alumnus.github }}" target="_blank">
                <i class="fab fa-github gh-icon"></i>
                </a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if alumnus.externalWebpage %}
    </a>
    {% elsif alumnus.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
</div>
