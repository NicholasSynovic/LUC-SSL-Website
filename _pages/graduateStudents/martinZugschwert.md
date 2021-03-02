---
layout: profile
profile:
 align: right
 image: martinZugschwert.jpg
title: Martin Zugschwert
description: Martin Zugschwert's Webpage
importance: 1
permalink: /graduateStudents/martinZugschwert/
---

## About

Martin has been a member of SSL since his Junior year. He will receive his B.S. in Computer Science from Loyola University Chicago in December 2020. He will receive his M.S. in Computer Science from Loyola University Chicago in December 2021. He currently works as a Data Architect at iManage alongside his Masters’ studies and research.

## Education Background

- BS in Computer Science from Loyola University Chicago. Estimated Graduation: 2020
- MS in Computer Science from Loyola University Chicago. Estimated Graduation: 2021

## Research Interests

- Scalable Development
- Data Infrastructure
- Data Analytics
- Data Storage

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
