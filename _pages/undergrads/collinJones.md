---
layout: profile
permalink: /undergraduateStudents/collinJones

title: Collin Jones
img: /assets/img/collinJones
github: https://github.com/CJones217
linkedin: https://www.linkedin.com/in/the-real-collin-jones/
externalWebpage: https://collinjones.xyz/
resume:
---

## About

Collin Jones is a senior studying computer science and computer crime and forensics. His research currently includes structural metrics of software, with a focus on cyclomatic complexity. Collin is interested in internet privacy, network security, software design, and blockchain technologies.

## Education Background

- BS in Computer Science from Loyola University Chicago. Estimated Graduation: 2021
- Minor in Computer Crime and Forensics from Loyola University Chicago. Estimated Graduation: 2021

## Research Interests

- Structural Metrics
- Internet Privacy
- Tor

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
