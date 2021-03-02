---
layout: profile
permalink: /alumni/seanHiggins

title: Sean Higgins
img: /assets/img/seanHiggins.jpeg
github: https://github.com/sean-m-higgins
linkedin: https://www.linkedin.com/in/sean-m-higgins20/
externalWebpage: https://www.seanmh.com/
resume:
---

## About

Sean Higgins is now an Alumnus of Loyola University Chicago. While an undergrad, Sean focused his research on Machine Learning starting with a keyword classifier based on a small body of text to be used in the note-taking system ZettelGeist. As a graduate student, Sean led the ML team in an attempt to classify Github issues for the software project analysis project SoftwareMetrics. Sean also served as a Teaching Assistant during his time as a graduate student for the following courses: Database Programming, Operating Systems, Intermediate Object-Oriented Programming, and Machine Learning.

## Education Background

- BS in Computer Science from Loyola University Chicago. Graduated: 2019
- MS in Software Engineering from Loyola University Chicago. Graduated: 2020

## Professional and Community Affiliations

- President of Computer Science Student Advisory Council
- Member of Don’t Panic
- Member of ACM
- Member of IEEE

## Research Interests

- Machine Learning
- Data Science
- Natural Language Processing

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
