---
layout: page
title: Data
permalink: /data/
description:
nav: true
nav_order: 4
display_categories: []
horizontal: false
---

Visualizations, tables, and links to standalone data dashboards (such as [this one](https://rpubs.com/saurabh90/school-dashboard)) will be added here.

----

&nbsp;

<p>
Figure 1: Region-wise total applications to (figure on the left) and acceptance rate (figure on the right) at Pembroke College from 2019-21
</p>
<br/>
<p>
<img src="../assets/img/map1.png" alt="Maps" width="800"/>
</p>


<!-- pages/data.md -->
<div class="dashboards">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized dashboards -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_dashboards = site.dashboards | where: "category", category -%}
  {%- assign sorted_dashboards = categorized_dashboards | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_dashboards -%}
      {% include dashboards_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_dashboards -%}
      {% include dashboards.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display dashboards without categories -->
  {%- assign sorted_dashboards = site.dashboards | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_dashboards -%}
      {% include dashboards_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_dashboards -%}
      {% include dashboards.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
