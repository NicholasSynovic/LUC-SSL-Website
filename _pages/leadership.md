---
layout: page
title: leadership
permalink: /leadership/
description: Our current leaders list.
nav: true
social: true  # includes social icons at the bottom of the page
---

## Introduction

This page contains the current listing of SSL staff.

These members of SSL operate on the “business” side of the organization. Their jobs are varied, but they all share the same common goal of advancing SSL as one of Loyola University Chicago’s premier laboratories. In other words, they provide the leadership and direction needed to promote, grow, and improve SSL.

In the spirit of being true peers, we list all names in alphabetical order by last name.

## Faculty Leadership

---

{% assign staff = site.data.faculty | sort: "lastName" %}
{% assign team = site.data.team | sort: "lastName" %}

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

## Student Leadership

---

<!-- SSL Student Leadership Projects Grid -->
<div class="projects grid">
  {% for leader in team %}
  {% if leader.section.studentLeadership %}
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
          <p class="card-text">{{ leader.titles.studentLeadership }}</p>
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

## Leadership Structure

The structure of SSL is written out in [this PDF document](/assets/pdf/Software_Systems_Laboratory_Leadership_Structure.pdf).

This document contains all information one may need to know about the different positions and their respected roles within SSL, the organization structure, as well as the application to apply for any of the roles listed within the document.

As a fairly new organization, we are still improving how SSL operates. As such, this document is subject to change in the future, and should be referred back to after such a change is made.
