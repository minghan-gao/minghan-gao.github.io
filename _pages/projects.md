---
layout: page
title: projects
permalink: /projects/
description: Selected course and independent projects in accessible interaction and wearable computing.
nav: true
nav_order: 3
---

These projects show how I move from a human need to an interactive prototype and evaluation. Select a card for the full process and outcomes.

<div class="projects">
  <div class="row row-cols-1 row-cols-md-2">
    {% assign class_projects = site.projects | where: "category", "project" | sort: "importance" %}
    {% for project in class_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>
