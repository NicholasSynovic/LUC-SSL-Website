---
layout: page
permalink: /team/
nav: true

title: team
description: Our current team list.
---

## Grad Students

---

{% assign team = site.data.team | sort: "lastName" %}

<!-- Graduate Students Projects Grid -->
<div class="projects grid">
  {% for grad in team %}
  {% if grad.section.graduateStudent%}
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
          <p class="card-text">{{ grad.titles.default }}</p>
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
</div>
<br>

## Undergrads

---

<!-- Undergraduate Students Projects Grid -->
<div class="projects grid">
  {% for undergrad in team %}
  {% if undergrad.section.undergraduateStudent%}
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
          <p class="card-text">{{ undergrad.titles.default }}</p>
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
</div>
