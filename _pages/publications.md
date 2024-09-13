---
layout: page
permalink: /publications/
title: Publications
description:  # [Google Scholar profile](https://scholar.google.com/citations?user=L1NLrxoAAAAJ)
years0: [2024]
years1: [2024, 2022, 2021] #[1967, 1956, 1950, 1935, 1905]
years2: [2020, 2019] #[1967, 1956, 1950, 1935, 1905]
nav: true
nav_order: 1
---
[Google Scholar profile](https://scholar.google.com/citations?user=L1NLrxoAAAAJ)



### **Submitted**
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years0 %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprints -q @*[year={{y}}]* %}
{% endfor %}

</div>


### **Peer-reviewed**
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years1 %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>


### **Other publications**
<div class="publications">

{%- for y in page.years2 %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papersother -q @*[year={{y}}]* %}
{% endfor %}

</div>



<!-- _pages/publications.md -->
<!-- <div class="publications"> -->

<!-- {%- for y in page.years %} -->
<!--   <h2 class="year">{{y}}</h2> -->
<!--   {% bibliography -f papers -q @*[year={{y}}]* %} -->
<!-- {% endfor %} -->

<!-- </div> -->


