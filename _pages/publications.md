---
layout: page
permalink: /papers/
title: papers
description: These are my finished papers in chronological order. (They are expository research so far, but there is more original research to come.)
years: [2022]
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
