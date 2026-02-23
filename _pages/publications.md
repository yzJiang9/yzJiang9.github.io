---
layout: page
permalink: /publications/
title: Publications
description:
years: [2026,2025,2024,2023,2022]
years_pre: [2025,2023]
nav: true
nav_order: 1
---

<div class="publications">

<h1>Preprints</h1>
{% for y in page.years_pre %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprints -q @*[year={{y}}]* %}
{% endfor %}

<h1>Peer-reviewed Paper</h1>
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
