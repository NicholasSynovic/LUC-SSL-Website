---
layout: profile
permalink: /graduateStudents/sophieVonHatten

title: Sophie Von Hatten
img: /assets/img/user.jpg
github: https://github.com/svonhatten
linkedin: https://www.linkedin.com/in/sophie-von-hatten-9863a018b/
externalWebpage:
resume:
---

## About

Sophie is a Front-end Software Engineer currently in her 1st year as a Graduate student at Loyola University Chicago for an MS in Software Engineering. As a member of SSL since her senior year as an undergraduate student at Loyola, she has been a part of the Metrics Dashboard team, her contributions including the front-end design and development of the visual data representation. Also, she now resides as a co-administrator for SSL as a whole. Her duties as such include managing and maintaining the organization from a student standpoint.

## Education Background

- BS in Software Engineering from Loyola University Chicago. Graduated: 2020
- MS in Software Engineering from Loyola University Chicago. Estimated Graduation: 2022

## Research Interests

- Front-End UI/UX Design
- Data Visualizations and Representations

## Research Projects

{% assign splitTitle = page.title | split: " " %}
{% assign lastName = splitTitle[1] %}
{% assign firstName = splitTitle[0] %}
{% assign projects = site.data.projects %}
{% assign team = site.data.team %}

{% for member in team %}
{% if member.lastName == lastName %}
{% if member.firstName == firstName %}
<div class="projects grid">
  <div class="grid-item">
    {% if member.associatedProjects %}
    {% for associatedProject in member.associatedProjects %}
    {% for project in projects %}
    {% if associatedProject == project.projectName %}
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
    {% endif %}
    {% endfor %}
    {% endfor %}
    {% endif %}
  </div>
</div>
{% endif %}
{% endif %}
{% endfor %}
