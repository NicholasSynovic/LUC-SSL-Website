---
layout: profile
title: Allan Miller
description: Allan Miller's Webpage
profile:
 align: right
 image: allanMiller.jpeg
importance: 1
permalink: /alumni/allanMiller
---

## About

Software Engineer at Ensighten Inc.

## Education Background

- MS in Computer Science from Loyola University Chicago. Graduated: 2020

## Professional and Community Affiliations

- Member of ACM
- Member of IEEE
- Member of ACS
- Member of AICHE

## Research Interests

- Machine Learning
- Software Systems
- Computer Science Education
- Software Workflows

## Research Projects

{% assign splitTitle = page.title | split: " " %}
{% assign lastName = splitTitle[1] %}
{% assign firstName = splitTitle[0] %}
{% assign projects = site.data.projects %}
{% assign team = site.data.team %}

{% if team.lastName == lastName %}
{% if team.firstName == firstName %}
<div class="projects grid">
  <div class="grid-item">
    {% if team.associatedProjects %}
    {% for project in team.associatedProjects %}
    {% if lastName %}
    <a href="{{ project.redirect }}" target="_blank">
    {% else %}
    <a href="{{ project.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if project.img %}
        <img src="{{ project.img | relative_url }}" alt="project thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase">{{ project.title }}</h2>
          <p class="card-text">{{ project.description }}</p>
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
    {% endfor %}
    {% endif %}
  </div>
</div>
{% endif %}
{% endif %}
