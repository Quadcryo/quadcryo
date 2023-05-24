---
layout: page
title: a small ap statistics project
description: here we investigated whether doing math because it is fun has an association with average confidence in solving math problems among high school students
img: stats_paper_matias_kyle.png
importance: 2
category: work
---

<!-- _projects/stats project.md -->
<div class="projects">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
