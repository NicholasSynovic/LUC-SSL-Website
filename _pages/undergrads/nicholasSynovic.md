---
layout: profile
permalink: /undergraduateStudents/nicholasSynovic

title: Nicholas Synovic
img: /assets/img/nicholasSynovic.png
github: https://github.com/NicholasSynovic
linkedin: https://linkedin.com/in/nsynovic
externalWebpage: https://loyolachicagocs.github.io/ssl/members/undergraduate-researchers-pages/nicholassynovic.github.io/
resume: https://nicholassynovic.github.io/assets/Nicholas_Synovic-Resume.pdf
---

## About

Nicholas Synovic is an undergraduate researcher working with SSL as a Team Lead and Software Engineer for the back-end portion of the Metrics Dashboard project, the current web maintainer for SSL, and as an Admin for the group. Furthermore, he is a part of the Chicago Area Undergraduate Research Inter-School Board, and the Loyola University Chicago Eta Omega Chapter of Beta Theta Pi as their Vice President of Communications. While taking on this load, Nicholas is also pursuing a bachelor’s degree in Computer Science and intends to pursue a Master’s degree in the same field.

## Education Background

- BS in Computer Science from Loyola University Chicago. Estimated Graduation: 2022

## Professional and Community Affiliations

- Vice President of Communications for the Eta Omega Chapter of Beta Theta Pi
- Board Member of the Chicago Area Undergradute Research Symposium Inter-School Board
- Member of Don’t Panic!
- Member of ACM

## Research Interests

- Web Scraping and Data Collection, Parsing, and Analyzing
- Portable Systems
- Politically Focussed Computer Science and Data Analytics
- User Experiences
- Accessibility Software



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
