---
layout: page
permalink: /publications/
title: Publications
description: "Conference papers and technical articles."
nav: true
nav_order: 1
---

[Google Scholar](https://scholar.google.co.kr/citations?user=Yul10xcAAAAJ&hl=en)

{% include bib_search.liquid %}

## International Conference Papers

<div class="publications">
{% bibliography --template bib_publications --query @*[category=international] %}
</div>

## Domestic Conference Papers

<div class="publications">
{% bibliography --template bib_publications --query @*[category=domestic] %}
</div>

## Technical Articles

<div class="publications">
{% bibliography --template bib_publications --query @*[category=technical] %}
</div>
