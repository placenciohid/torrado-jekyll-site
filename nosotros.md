---
title: Nosotros
layout: page
description: "Conoce al equipo de Torrado Equipment. Más de 20 años especializados en maquinaria agrícola en Puerto Rico. Familia, experiencia y compromiso."
bodyClass: page-nosotros
---

## Quiénes Somos

Por más de 20 años nos hemos especializado en la venta y reparación de equipos agrícolas de primera calidad. Con nuestra experiencia y dedicación, buscamos proporcionar a los agricultores herramientas confiables que optimicen la productividad y el rendimiento de su operación agrícola.

## Nuestro Equipo

<div class="row justify-content-center mt-5">
  {% assign team_members = site.team | sort: 'weight' %}
  {% for member in team_members %}
    <div class="col-12 col-md-6 col-lg-3 mb-4">
      <div class="team-card-enhanced animate-on-scroll">
        {% if member.image %}
          <div class="team-card-image">
            <img alt="{{ member.title }}" src="{{ member.image | relative_url }}" loading="lazy" />
          </div>
        {% endif %}
        <div class="team-card-body">
          <h3 class="team-card-name">{{ member.title }}</h3>
          <span class="team-card-role">{{ member.jobtitle }}</span>
          {% if member.content != "" %}
            <div class="team-card-bio">
              {{ member.content }}
            </div>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>
