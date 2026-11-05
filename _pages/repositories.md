---
layout: page
permalink: /repositorios/
title: repositorios
description: El código de mis proyectos, disponible en GitHub.
nav: true
nav_order: 3
---

<div class="projects">
  {% for repo in site.data.repositories.repositorios %}
    <div class="card repo-tarjeta">
      <div class="card-body">
        <a href="{{ repo.url }}">
          <h2 class="card-title">{{ repo.nombre }}</h2>
        </a>
        <p class="card-text">{{ repo.descripcion }}</p>
        <p class="card-text"><strong>Lenguaje:</strong> {{ repo.lenguaje }}</p>
      </div>
    </div>
  {% endfor %}
</div>

[Ver mi perfil completo en GitHub](https://github.com/dgarcesg)
