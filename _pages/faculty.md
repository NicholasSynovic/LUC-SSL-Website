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

<!-- SSL Faculty Leadership Projects Grid -->
<div class="projects grid">
  {% assign sorted_faculty = site.data.faculty %}
  {% for faculty in sorted_faculty %}
  {% if faculty.gradeLevel == "Faculty Leadership" %}
  <div class="grid-item">
    {% if faculty.redirect %}
    <a href="{{ faculty.redirect }}" target="_blank">
    {% else %}
    <a href="{{ faculty.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if faculty.img %}
        <img src="{{ faculty.img | relative_url }}" alt="faculty thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ faculty.first | append: " " | append: faculty.last }}</h5>
          <p class="card-text">{{ faculty.title }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if faculty.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ faculty.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Student Leadership

---

<!-- SSL Faculty Leadership Projects Grid -->
<div class="projects grid">
  {% assign sorted_faculty = site.data.faculty %}
  {% for faculty in sorted_faculty %}
  {% if faculty.gradeLevel == "Student Leadership" %}
  <div class="grid-item">
    {% if faculty.redirect %}
    <a href="{{ faculty.redirect }}" target="_blank">
    {% else %}
    <a href="{{ faculty.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if faculty.img %}
        <img src="{{ faculty.img | relative_url }}" alt="faculty thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ faculty.first | append: " " | append: faculty.last }}</h5>
          <p class="card-text">{{ faculty.title }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if faculty.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ faculty.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Faculty Advisors

---

<!-- Alumna Projects Grid -->
<div class="projects grid">
  {% assign sorted_faculty = site.data.faculty %}
  {% for faculty in sorted_faculty %}
  {% if faculty.gradeLevel == "Faculty Advisor" %}
  <div class="grid-item">
    {% if faculty.redirect %}
    <a href="{{ faculty.redirect }}" target="_blank">
    {% else %}
    <a href="{{ faculty.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if faculty.img %}
        <img src="{{ faculty.img | relative_url }}" alt="faculty thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ faculty.first | append: " " | append: faculty.last }}</h5>
          <p class="card-text">{{ faculty.title }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if faculty.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ faculty.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Argonne National Laboratory Collaborators

---

<!-- Argonne National Laboratory Collaborators Projects Grid -->
<div class="projects grid">
  {% assign sorted_faculty = site.data.faculty %}
  {% for faculty in sorted_faculty %}
  {% if faculty.gradeLevel == "Argonne National Laboratory Collaborators" %}
  <div class="grid-item">
    {% if faculty.redirect %}
    <a href="{{ faculty.redirect }}" target="_blank">
    {% else %}
    <a href="{{ faculty.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if faculty.img %}
        <img src="{{ faculty.img | relative_url }}" alt="faculty thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ faculty.first | append: " " | append: faculty.last }}</h5>
          <p class="card-text">{{ faculty.title }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if faculty.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ faculty.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Louisiana State University Collaborators

---

<!-- Louisiana State University Collaborators Projects Grid -->
<div class="projects grid">
  {% assign sorted_faculty = site.data.faculty %}
  {% for faculty in sorted_faculty %}
  {% if faculty.gradeLevel == "Louisiana State University Collaborators" %}
  <div class="grid-item">
    {% if faculty.redirect %}
    <a href="{{ faculty.redirect }}" target="_blank">
    {% else %}
    <a href="{{ faculty.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if faculty.img %}
        <img src="{{ faculty.img | relative_url }}" alt="faculty thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ faculty.first | append: " " | append: faculty.last }}</h5>
          <p class="card-text">{{ faculty.title }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if faculty.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ faculty.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Outside Ph.D. Student Collaborators

---

<!-- Outside Ph.D. Student Collaborators Projects Grid -->
<div class="projects grid">
  {% assign sorted_faculty = site.data.faculty %}
  {% for faculty in sorted_faculty %}
  {% if faculty.gradeLevel == "Outside Ph.D. Student Collaborators" %}
  <div class="grid-item">
    {% if faculty.redirect %}
    <a href="{{ faculty.redirect }}" target="_blank">
    {% else %}
    <a href="{{ faculty.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if faculty.img %}
        <img src="{{ faculty.img | relative_url }}" alt="faculty thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ faculty.first | append: " " | append: faculty.last }}</h5>
          <p class="card-text">{{ faculty.title }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if faculty.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ faculty.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## Purdue University Collaborators

---

<!-- Purdue University Collaborators Projects Grid -->
<div class="projects grid">
  {% assign sorted_faculty = site.data.faculty %}
  {% for faculty in sorted_faculty %}
  {% if faculty.gradeLevel == "Purdue University Collaborators" %}
  <div class="grid-item">
    {% if faculty.redirect %}
    <a href="{{ faculty.redirect }}" target="_blank">
    {% else %}
    <a href="{{ faculty.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if faculty.img %}
        <img src="{{ faculty.img | relative_url }}" alt="faculty thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ faculty.first | append: " " | append: faculty.last }}</h5>
          <p class="card-text">{{ faculty.title }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if faculty.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ faculty.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
<br>

## University of Alabama Collaborators Collaborators

---

<!-- University of Alabama Collaborators Projects Grid -->
<div class="projects grid">
  {% assign sorted_faculty = site.data.faculty %}
  {% for faculty in sorted_faculty %}
  {% if faculty.gradeLevel == "University of Alabama Collaborators" %}
  <div class="grid-item">
    {% if faculty.redirect %}
    <a href="{{ faculty.redirect }}" target="_blank">
    {% else %}
    <a href="{{ faculty.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if faculty.img %}
        <img src="{{ faculty.img | relative_url }}" alt="faculty thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ faculty.first | append: " " | append: faculty.last }}</h5>
          <p class="card-text">{{ faculty.title }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if faculty.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ faculty.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
  {% endif %}
{% endfor %}
</div>
<br>
