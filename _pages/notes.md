---
layout: page
title: Notes
permalink: /notes/
nav: true
nav_order: 4
horizontal: false
---

<!-- pages/notss.md -->
<div class="projects">
<!-- Display projects without categories -->

{% assign sorted_notes = site.notes | sort: "importance" %}

  <!-- Generate cards for each project -->

{%- if page.horizontal -%}
    <div class="container">
      <div class="row row-cols-1 row-cols-md-2">
        {%- for project in sorted_notes -%}
          {%- include projects_horizontal.liquid -%}
        {%- endfor -%}
      </div>
    </div>
  {%- else -%}
    <div class="row row-cols-1 row-cols-md-3">
      {%- for project in sorted_notes -%}
        {%- include projects.liquid -%}
      {%- endfor -%}
    </div>
  {%- endif -%}
</div>
