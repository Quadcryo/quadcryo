---
layout: page
permalink: /publications/
title: publications
description: recent papers and publications
years: [2022]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">A Brief Introduction to Bézier Curves</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={Summer 2022}]* %}
{% endfor %}

</div>

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">An Introduction to Algebraic Numbers and Algebraic Integers</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">On the Value of the Quadratic Gauss Sum</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">Proofs and Applications of Quadratic Reciprocity</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>
