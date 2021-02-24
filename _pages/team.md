---
layout: page
title: team
permalink: /team/
description: Our current team list.
nav: true
---

## Student Leaders

---

## Undergrads

---

## Grads

---

## Alumni

---
<!-- Alumni Projects Grid -->
<div class="projects grid">
  {% assign sorted_alumni = site.data.alumni %}
  {% for alumni in sorted_alumni %}
  <div class="grid-item">
    {% if alumni.redirect %}
    <a href="{{ alumni.redirect }}" target="_blank">
    {% else %}
    <a href="{{ alumni.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if alumni.img %}
        <img src="{{ alumni.img | relative_url }}" alt="alumni thumbnail">
        {% endif %}
        <div class="card-body">
          <h5>{{ alumni.first | append: " " | append: alumni.last }}</h5>
          <p class="card-text">{{ alumni.title }}</p>

          <div class="row ml-1 mr-1 p-0">
            {% if alumni.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="GitHub Profile">
                <a href="{{ alumni.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
