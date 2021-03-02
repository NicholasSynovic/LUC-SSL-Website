---
layout: profile
permalink: /undergraduateStudents/treyRoche

title: Trey Roche
img: /assets/img/treyRoche.jpg
github: https://github.com/Troche4
linkedin: https://www.linkedin.com/in/trey-roche-587b7717a/
externalWebpage: http://treyroche.com/
resume: /assets/docs/ResumeTreyRoche-Trey_Roche.docx
---

## About

Trey is an undergraduate researcher at SSL pursuing a B.S. in Computer Science. He is currently leading the Color Deficiency Correction Project at SSL. His research interests include web development, distributed systems, and promoting accessible development.

## Education Background

- BS in Computer Science from Loyola University Chicago. Estimated Graduation: 2021

## Research Interests

- Web Development
- Distributed Systems
- Promoting Accessible Development

## Research Projects

{% assign splitTitle = page.title | split: " " %}
{% assign lastName = splitTitle[1] %}
{% assign firstName = splitTitle[0] %}
{% assign projects = site.data.projects | sort: "projectName" %}
{% assign team = site.data.team | sort: "lastName" %}

<div class="projects grid">
{% for member in team %}
{% if member.lastName == lastName %}
{% if member.firstName == firstName %}
  {% if member.associatedProjects %}
  {% for associatedProject in member.associatedProjects %}
  {% for project in projects %}
  {% if associatedProject == project.projectName %}
  <div class="grid-item">
    <a href="{{ project.webpage | relative_url }}">
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase">{{ project.projectName }}</h2>
          <p class="card-text">{{ project.shortDescription }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if project.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ project.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if project.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ project.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
  {% endfor %}
  {% endfor %}
  {% endif %}
</div>
{% endif %}
{% endif %}
{% endfor %}
