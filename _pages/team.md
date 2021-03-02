---
layout: page
title: team
permalink: /team/
description: Our current team list.
nav: true
social: true  # includes social icons at the bottom of the page
---

## Grad Students

---

{% assign team = site.data.team %}

<!-- Grad Students Projects Grid -->
<div class="projects grid">
  {% for grad in team %}
  {% if grad.section.graduateStudent%}
  <div class="grid-item">
    {% if grad.externalWebpage %}
    <a href="{{ grad.externalWebpage }}" target="_blank">
    {% else %}
    <a href="{{ grad.webpage | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if grad.img %}
        <img src="{{ grad.img | relative_url }}" alt="grad thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ grad.firstName | append: " " | append: grad.lastName }}</h5>
          <p class="card-text">{{ grad.titles.default }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if grad.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ grad.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Undergrads

---

<!-- Grad Students Projects Grid -->
<div class="projects grid">
  {% assign sorted_team = site.data.team %}
  {% for team in sorted_team %}
  {% if team.gradeLevel == "Undergraduate" %}
  <div class="grid-item">
    {% if team.redirect %}
    <a href="{{ team.redirect }}" target="_blank">
    {% else %}
    <a href="{{ team.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if team.img %}
        <img src="{{ team.img | relative_url }}" alt="team thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ team.first | append: " " | append: team.last }}</h5>
          <p class="card-text">{{ team.title }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if team.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ team.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
