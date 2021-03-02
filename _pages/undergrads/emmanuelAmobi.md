---
layout: profile
title: Emmanuel Amobi
description: Emmanuel Amobi's Webpage
profile:
 align: right
 image: user.jpg
importance: 1
permalink: /undergraduateStudents/emmanuelAmobi
---

## About

Emmanuel is currently a senior majoring in software engineering with a minor in Mathematics. He is currently researching the metrics dashboard in a research group at Loyola known as SSL. He is also a member of the DON’T PANIC club, at computer science club at Loyola that hosts a lot of computer science events. He has worked with various students and professors at the Loyola Computer Science Tutoring Department, aiding students with CS-related topics and giving them the needed assistance. In his free time, he likes to work out, watch youtube videos on a variety of topics of interest and likes to read research papers and books on nutrition and psychology.

## Education Background

- BS in Software Engineering from Loyola University Chicago. Estimated Graduation: 2021
- Minor in Mathematics from Loyola University Chicago. Estimated Graduation: 2021

## Professional and Community Affiliations

- Member of Don’t Panic!

## Research Interests

- Effective Planning and Decision Making
- Open Source Software Development
- Programming Tools and Environments

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
