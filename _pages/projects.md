---
layout: page
permalink: /projects/
nav: true

title: projects
description: Our current list of in progress and incubating research endeavours
---

{% assign projects = site.data.projects | sort: "projectName" %}

## In Progress

---

<div class="projects grid">
  {% for project in projects %}
  {% if project.status == "In Progress" %}
  <div class="grid-item">
    {% if project.webpage %}
    <a href="{{ project.webpage | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title">{{ project.projectName }}</h2>
          <p class="card-text">{{ project.shortDescription }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if project.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if project.webpage %}
    </a>
    {% endif %}
  </div>
{% endif %}
{% endfor %}
</div>
<br>

## Incubating

---

<div class="projects grid">
  {% for project in projects %}
  {% if project.status == "Incubating" %}
  <div class="grid-item">
    {% if project.webpage %}
    <a href="{{ project.webpage | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title">{{ project.projectName }}</h2>
          <p class="card-text">{{ project.shortDescription }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if project.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if project.webpage %}
    </a>
    {% endif %}
  </div>
{% endif %}
{% endfor %}
</div>
<br>
