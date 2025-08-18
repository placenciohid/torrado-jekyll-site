---
title: Nosotros
layout: page
description: Conoce nuestro equipo y nuestra historia
bodyClass: page-nosotros
---

## QUIENES SOMOS

Por más de 20 años nos hemos especializado en la venta y reparación de equipos agrícolas de primera calidad. Con nuestra experiencia y dedicación, buscamos proporcionar a los agricultores herramientas confiables que optimicen la productividad y el rendimiento de su operación agrícola.

## NUESTRO EQUIPO

<div class="row justify-content-center mt-5">
  {% assign team_members = site.team | sort: 'weight' %}
  {% for member in team_members %}
    <div class="col-12 col-md-6 col-lg-3 mb-4">
      <div class="team-member text-center">
        {% if member.image %}
          <div class="team-image mb-3">
            <img alt="{{ member.title }}" class="img-fluid rounded-circle" src="{{ member.image | relative_url }}" style="width: 150px; height: 150px; object-fit: cover;" />
          </div>
        {% endif %}
        <div class="team-meta">
          <h3 class="team-name">{{ member.title }}</h3>
          <p class="team-description">{{ member.jobtitle }}</p>
          {% if member.content %}
            <div class="team-content">
              {{ member.content }}
            </div>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>