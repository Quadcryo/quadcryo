---
layout: page
permalink: /papers/
title: papers
description: These are my finished papers in chronological order. (These are expository research so far, but original research comes with time.)
years: [2022, 2023]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
