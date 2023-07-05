---
layout: page
permalink: /publications/
title: Publications
description:
years: [2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010, 2009, 2008, 2007, 2006, 2005, 2004, 2003, 2002, 2001, 2000]
nav: true
nav_order: 5
---

&nbsp;

#### Peer-reviewed papers

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>

&nbsp;

#### Books

<div class="publications">

{%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f books -q @*[year={{y}}]* %}
{% endfor %}

</div>

&nbsp;

#### Book chapters

<div class="publications">

{%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f chapters -q @*[year={{y}}]* %}
{% endfor %}

</div>

&nbsp;

#### Datasets

<div class="publications">

{%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f datasets -q @*[year={{y}}]* %}
{% endfor %}

</div>

&nbsp;

#### Preprints

<div class="publications">

{%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f preprints -q @*[year={{y}}]* %}
{% endfor %}

</div>

&nbsp;

#### Conference proceedings

<div class="publications">

{%- for y in page.years %}
  <!-- <h2 class="year">{{y}}</h2> -->
  {% bibliography -f conferences -q @*[year={{y}}]* %}
{% endfor %}

</div>

