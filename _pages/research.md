---
layout: page
title: research
permalink: /research/
description: Research across interactive systems, wearable sensing, accessibility, and human-centered AI.
nav: true
nav_order: 2
---

My research asks how sensing and AI systems can provide useful, respectful support in everyday contexts. Select a project to see the research question, methods, and my contribution.

<div class="projects">
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
      {% assign research_projects = site.projects | where: "category", "research" | sort: "importance" %}
      {% for project in research_projects %}
        {% include projects_horizontal.liquid %}
      {% endfor %}
    </div>
  </div>
</div>
