---
layout: page
title: Research
permalink: /projects/
description: "Security and trust for aerial networks and interoperable Counter-UAS systems."
nav: true
nav_order: 2
---

My research focuses on the security and reliability of aerial and mobile network infrastructure. I investigate UxNB security and positioning, trust mechanisms for Open RAN, and interoperability requirements for Counter-UAS systems.

## Research areas

<div class="projects">
  {% assign research_projects = site.projects | where: "research", true | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in research_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>

For published papers, granted patents, and standards under development, see [Publications]({{ '/publications/' | relative_url }}).
