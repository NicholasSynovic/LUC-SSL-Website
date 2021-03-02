---
layout: page
permalink: /projects/sslWebsite
title: SSL Website
description: The SSL Website
---

{% assign staff = site.data.faculty | sort: "lastName" %}
{% assign team = site.data.team | sort: "lastName" %}

## Introduction

To promote both the laboratory and research done by the researchers, faculty, and collaborators of the Software and Systems Laboratory (SSL), this website was developed. This website has been built several times. Once with the Python Sphinx library with the ReadTheDocs theme, and currently with the Ruby Jekyll library with the Al-Folio theme.

## Web Site

- [SSL Website](https://ssl.cs.luc.edu)

## Source Code

- [Source Code](https://github.com/loyolachicagocs/ssl2)

## Prototypes

- [Old Site (Hosted on GitHub Pages)](https://loyolachicagocs.github.io/ssl)
- [Old Site Source Code](https://github.com/loyolachicagocs/ssl)

## Faculty Advisors

<!-- SSL Faculty advisorship Projects Grid -->
<div class="projects grid">
  {% for advisor in staff %}
  {% if advisor.section.facultyLeadership or advisor.section.facultyAdvisor %}
  {% for project in advisor.associatedProjects %}
  {% if project == page.title %}
  <div class="grid-item">
    {% if advisor.externalWebpage %}
    <a href="{{ advisor.externalWebpage }}" target="_blank">
    {% elsif advisor.webpage %}
    <a href="{{ advisor.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if advisor.img %}
        <img src="{{ advisor.img | relative_url }}" alt="advisor thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ advisor.firstName | append: " " | append: advisor.lastName }}</h5>
          <div class="row ml-1 mr-1 p-0">
            {% if advisor.socials.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ advisor.socials.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if advisor.externalWebpage %}
    </a>
    {% elsif advisor.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
  {% endfor %}
  {% endif %}
  {% endfor %}
</div>
<br>

## Former Researchers

<div class="projects grid">
  {% for formerResearcher in team %}
  {% if formerResearcher.section.alumna or formerResearcher.section.alumnus %}
  {% for project in formerResearcher.associatedProjects %}
  {% if project == page.title %}
  <div class="grid-item">
    {% if formerResearcher.externalWebpage %}
    <a href="{{ formerResearcher.externalWebpage }}" target="_blank">
    {% elsif formerResearcher.webpage %}
    <a href="{{ formerResearcher.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if formerResearcher.img %}
        <img src="{{ formerResearcher.img | relative_url }}" alt="formerResearcher thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ formerResearcher.firstName | append: " " | append: formerResearcher.lastName }}</h5>
          <div class="row ml-1 mr-1 p-0">
            {% if formerResearcher.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ formerResearcher.github }}" target="_blank">
                <i class="fab fa-github gh-icon"></i>
                </a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if formerResearcher.externalWebpage %}
    </a>
    {% elsif formerResearcher.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
{% endif %}
{% endfor %}
</div>
<br>

## Graduate Researchers

<!-- Graduate Students Projects Grid -->
<div class="projects grid">
  {% for grad in team %}
  {% if grad.section.graduateStudent %}
  {% for project in grad.associatedProjects %}
  {% if project == page.title %}
  <div class="grid-item">
    {% if grad.externalWebpage %}
    <a href="{{ grad.externalWebpage }}" target="_blank">
    {% elsif grad.webpage %}
    <a href="{{ grad.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if grad.img %}
        <img src="{{ grad.img | relative_url }}" alt="grad thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ grad.firstName | append: " " | append: grad.lastName }}</h5>
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
    {% if grad.externalWebpage %}
    </a>
    {% elsif grad.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
{% endif %}
{% endfor %}
</div>
<br>

## Undergraduate Researchers

<!-- Undergraduate Students Projects Grid -->
<div class="projects grid">
  {% for undergrad in team %}
  {% if undergrad.section.undergraduateStudent %}
  {% for project in undergrad.associatedProjects %}
  {% if project == page.title %}
  <div class="grid-item">
    {% if undergrad.externalWebpage %}
    <a href="{{ undergrad.externalWebpage }}" target="_blank">
    {% elsif undergrad.webpage %}
    <a href="{{ undergrad.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if undergrad.img %}
        <img src="{{ undergrad.img | relative_url }}" alt="undergrad thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ undergrad.firstName | append: " " | append: undergrad.lastName }}</h5>
          <div class="row ml-1 mr-1 p-0">
            {% if undergrad.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ undergrad.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if undergrad.externalWebpage %}
    </a>
    {% elsif undergrad.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
{% endif %}
{% endfor %}
</div>
<br>

## Collaborations

<!-- Collaborator Projects Grid -->
<div class="projects grid">
  {% for collaborator in staff %}
  {% if collaborator.section.other %}
  {% for project in collaborator.associatedProjects %}
  {% if project == page.title %}
  <div class="grid-item">
    {% if collaborator.externalWebpage %}
    <a href="{{ collaborator.externalWebpage }}" target="_blank">
    {% elsif collaborator.webpage %}
    <a href="{{ collaborator.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if collaborator.img %}
        <img src="{{ collaborator.img | relative_url }}" alt="collaborator thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ collaborator.firstName | append: " " | append: collaborator.lastName }}</h5>
          <div class="row ml-1 mr-1 p-0">
            {% if collaborator.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ collaborator.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if collaborator.externalWebpage %}
    </a>
    {% elsif collaborator.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
{% endif %}
{% endfor %}
</div>
<br>
