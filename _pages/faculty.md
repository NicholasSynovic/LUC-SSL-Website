---
layout: page
title: faculty
permalink: /faculty/
description: Our current faculty list.
nav: true
social: true  # includes social icons at the bottom of the page
---

## Faculty Leadership

---

{% assign staff = site.data.faculty %}

<!-- SSL Faculty Leadership Projects Grid -->
<div class="projects grid">
  {% for leader in staff %}
  {% if leader.section.facultyLeadership %}
  <div class="grid-item">
    {% if leader.externalWebpage %}
    <a href="{{ leader.externalWebpage }}" target="_blank">
    {% elsif leader.webpage %}
    <a href="{{ leader.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if leader.img %}
        <img src="{{ leader.img | relative_url }}" alt="leader thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ leader.firstName | append: " " | append: leader.lastName }}</h5>
          <p class="card-text">{{ leader.titles.facultyLeadership }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if leader.socials.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ leader.socials.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if leader.externalWebpage %}
    </a>
    {% elsif leader.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Faculty Advisors

---

<!-- Faculty Advisors Projects Grid -->
<div class="projects grid">
  {% for advisor in staff %}
  {% if advisor.section.facultyAdvisor %}
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
          <p class="card-text">{{ advisor.titles.default }}</p>
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
</div>
<br>

## Argonne National Laboratory Collaborators

---

<!-- Argonne National Laboratory Collaborators Projects Grid -->
<div class="projects grid">
  {% for argonne in staff %}
  {% if argonne.section.other == "Argonne National Laboratory Collaborators" %}
  <div class="grid-item">
    {% if argonne.externalWebpage %}
    <a href="{{ argonne.externalWebpage }}" target="_blank">
    {% elsif argonne.webpage %}
    <a href="{{ argonne.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if argonne.img %}
        <img src="{{ argonne.img | relative_url }}" alt="argonne thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ argonne.firstName | append: " " | append: argonne.lastName }}</h5>
          <p class="card-text">{{ argonne.titles.default }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if argonne.socials.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ argonne.socials.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if argonne.externalWebpage %}
    </a>
    {% elsif argonne.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Louisiana State University Collaborators

---

<!-- Louisiana State University Collaborators Projects Grid -->
<div class="projects grid">
  {% for lsu in staff %}
  {% if lsu.section.other == "Louisiana State University Collaborators" %}
  <div class="grid-item">
    {% if lsu.externalWebpage %}
    <a href="{{ lsu.externalWebpage }}" target="_blank">
    {% elsif lsu.webpage %}
    <a href="{{ lsu.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if lsu.img %}
        <img src="{{ lsu.img | relative_url }}" alt="lsu thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ lsu.firstName | append: " " | append: lsu.lastName }}</h5>
          <p class="card-text">{{ lsu.titles.default }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if lsu.socials.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ lsu.socials.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if lsu.externalWebpage %}
    </a>
    {% elsif lsu.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Outside Ph.D. Student Collaborators

---

<!-- Outside Ph.D. Student Collaborators Projects Grid -->
<div class="projects grid">
  {% for phd in staff %}
  {% if phd.section.other == "Outside Ph.D. Student Collaborators" %}
  <div class="grid-item">
    {% if phd.externalWebpage %}
    <a href="{{ phd.externalWebpage }}" target="_blank">
    {% elsif phd.webpage %}
    <a href="{{ phd.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if phd.img %}
        <img src="{{ phd.img | relative_url }}" alt="phd thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ phd.firstName | append: " " | append: phd.lastName }}</h5>
          <p class="card-text">{{ phd.titles.default }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if phd.socials.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ phd.socials.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if phd.externalWebpage %}
    </a>
    {% elsif phd.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Purdue University Collaborators

---

<!-- Purdue University Collaborators Projects Grid -->
<div class="projects grid">
  {% for purdue in staff %}
  {% if purdue.section.other == "Purdue University Collaborators" %}
  <div class="grid-item">
    {% if purdue.externalWebpage %}
    <a href="{{ purdue.externalWebpage }}" target="_blank">
    {% elsif purdue.webpage %}
    <a href="{{ purdue.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if purdue.img %}
        <img src="{{ purdue.img | relative_url }}" alt="purdue thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ purdue.firstName | append: " " | append: purdue.lastName }}</h5>
          <p class="card-text">{{ purdue.titles.default }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if purdue.socials.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ purdue.socials.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if purude.externalWebpage %}
    </a>
    {% elsif purude.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## University of Alabama Collaborators Collaborators

---

<!-- University of Alabama Collaborators Projects Grid -->
<div class="projects grid">
  {% for alabama in staff %}
  {% if alabama.section.other == "University of Alabama Collaborators" %}
  <div class="grid-item">
    {% if alabama.externalWebpage %}
    <a href="{{ alabama.externalWebpage }}" target="_blank">
    {% elsif alabama.webpage %}
    <a href="{{ alabama.webpage | relative_url }}">
    {% else %}
    <!-- Do nothing -->
    {% endif %}
      <div class="card hoverable">
        {% if alabama.img %}
        <img src="{{ alabama.img | relative_url }}" alt="alabama thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ alabama.firstName | append: " " | append: alabama.lastName }}</h5>
          <p class="card-text">{{ alabama.titles.default }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if alabama.socials.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ alabama.socials.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    {% if alumnus.externalWebpage %}
    </a>
    {% elsif alumnus.webpage %}
    </a>
    {% else %}
    <!-- Do nothing -->
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
</div>
<br>
