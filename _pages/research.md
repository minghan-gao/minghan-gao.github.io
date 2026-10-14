---
layout: page
title: research
permalink: /research/
description: Wearable and health sensing, accessible interaction, and human-centered AI.
nav: true
nav_order: 2
---

<style>
  .research-list {
    margin-top: 2rem;
  }

  .research-entry {
    display: grid;
    grid-template-columns: minmax(0, 1fr);
    gap: 1.5rem;
    padding: 2rem 0;
    border-top: 1px solid var(--global-divider-color);
  }

  .research-entry.has-image {
    grid-template-columns: 240px minmax(0, 1fr);
  }

  .research-image {
    display: block;
    align-self: start;
    border-radius: 10px;
    overflow: hidden;
    background: var(--global-code-bg-color);
  }

  .research-image img {
    display: block;
    width: 100%;
    aspect-ratio: 4 / 3;
    object-fit: contain;
    transition: transform 180ms ease;
  }

  .research-image:hover img {
    transform: scale(1.025);
  }

  .research-meta,
  .research-people {
    font-size: 0.9rem;
    line-height: 1.6;
    color: var(--global-text-color-light);
    margin-bottom: 0.35rem;
  }

  .research-title {
    font-size: 1.45rem;
    font-weight: 500;
    line-height: 1.3;
    margin: 0.45rem 0 0.75rem;
  }

  .research-title a {
    color: var(--global-text-color);
    text-decoration: none;
  }

  .research-title a:hover {
    color: var(--global-theme-color);
  }

  .research-summary,
  .research-contribution {
    line-height: 1.65;
    margin-bottom: 0.65rem;
  }

  .research-contribution strong {
    font-weight: 500;
  }

  .research-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem 1.25rem;
    margin-top: 0.9rem;
    font-size: 0.9rem;
  }

  .research-entry a:focus-visible {
    outline: 2px solid var(--global-theme-color);
    outline-offset: 4px;
  }

  @media (max-width: 700px) {
    .research-entry.has-image {
      grid-template-columns: minmax(0, 1fr);
    }

    .research-image {
      width: 100%;
      max-width: 360px;
    }

    .research-title {
      font-size: 1.3rem;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .research-image img {
      transition: none;
    }
  }
</style>

<div class="research-list">
  {% assign research_projects = site.projects | where: "category", "research" | sort: "importance" %}
  {% for project in research_projects %}
    <article class="research-entry{% if project.img %} has-image{% endif %}">

      {% if project.img %}
        <a class="research-image"
           href="{{ project.url | relative_url }}"
           aria-label="{{ project.title | escape }}">
          <img src="{{ project.img | relative_url }}"
               alt="{{ project.image_alt | default: project.title | escape }}"
               loading="lazy">
        </a>
      {% endif %}

      <div class="research-content">
        <div class="research-meta">
          {{ project.period | escape }} · {{ project.institution | escape }}
        </div>

        <h2 class="research-title">
          <a href="{{ project.url | relative_url }}">
            {{ project.title | escape }}
          </a>
        </h2>

        {% if project.people %}
          <div class="research-people">
            {{ project.people | escape }}
          </div>
        {% endif %}

        <p class="research-summary">
          {{ project.description | escape }}
        </p>

        {% if project.contribution %}
          <p class="research-contribution">
            <strong>My contribution:</strong>
            {{ project.contribution | escape }}
          </p>
        {% endif %}

        <div class="research-links">
          <a href="{{ project.url | relative_url }}">Project details →</a>
          {% if project.paper_url %}
            <a href="{{ project.paper_url | escape }}">Paper ↗</a>
          {% endif %}
          {% if project.demo_url %}
            <a href="{{ project.demo_url | escape }}">Demo ↗</a>
          {% endif %}
        </div>
      </div>

    </article>
  {% endfor %}
</div>