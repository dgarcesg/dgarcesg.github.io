---
layout: page
title: proyectos
permalink: /proyectos/
description: Mis proyectos de ciencia de datos, cada uno con su pregunta, su resultado y su código.
nav: true
nav_order: 2
---

{% assign proyectos = site.projects | sort: "importance" %}

<div class="projects">
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in proyectos %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>
