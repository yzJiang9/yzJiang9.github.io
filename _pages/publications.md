---
layout: page
permalink: /publications/
title: Publications
description:
years: [2023,2022]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

 <h1>Pre-prints</h1>
{% for y in page.years_pre %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprints -q @*[year={{y}}]* %}
{% endfor %}
  
  
 <h1>Peer-reviewed Publication</h1> 
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>
