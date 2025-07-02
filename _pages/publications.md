---
layout: page
permalink: /articles/
title: Articles
description: Original research papers. (E) indicates that a paper is expository.
years: [2025, 2024, 2023, 2022]
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
