---
title: Nuestro Equipo
layout: modern-page
header_title: "Conoce al Equipo"
description: "Conoce al equipo de Torrado Equipment. Más de 20 años especializados en maquinaria agrícola en Puerto Rico. Familia, experiencia y compromiso."
---

<div style="text-align: center; max-width: 800px; margin: 0 auto var(--space-12);">
  <span class="section-label">Nuestro Equipo</span>
  <h2 style="margin-bottom: var(--space-4);">La Familia Torrado Equipment</h2>
  <p style="font-size: 1.125rem; color: var(--color-text-light);">
    Por más de 20 años nos hemos especializado en la venta y reparación de equipos agrícolas de primera calidad. 
    Con nuestra experiencia y dedicación, buscamos proporcionar a los agricultores herramientas confiables 
    que optimicen la productividad y el rendimiento de su operación agrícola.
  </p>
</div>

<div class="team-grid">
  {% assign team_members = site.team | sort: 'weight' %}
  {% for member in team_members %}
    <div class="team-card">
      {% if member.image %}
        <div class="team-card-image">
          <img alt="{{ member.title }}" src="{{ member.image | relative_url }}" loading="lazy" />
        </div>
      {% endif %}
      <div class="team-card-body">
        <h3>{{ member.title }}</h3>
        <p class="role">{{ member.jobtitle }}</p>
        {% if member.content != "" %}
          <div style="margin-top: var(--space-4); color: var(--color-text-light); font-size: 0.9375rem;">
            {{ member.content }}
          </div>
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>

<div style="background: var(--color-gray-50); border-radius: var(--radius-2xl); padding: var(--space-12); margin-top: var(--space-16);">
  <div style="text-align: center; max-width: 700px; margin: 0 auto;">
    <span class="section-label">Únete al Equipo</span>
    <h2 style="margin-bottom: var(--space-4);">¿Quieres Ser Parte de Nuestra Familia?</h2>
    <p style="color: var(--color-text-light); margin-bottom: var(--space-8);">
      Siempre estamos buscando personas apasionadas por la agricultura y el servicio al cliente. 
      Si te interesa formar parte de nuestro equipo, contáctanos.
    </p>
    <a href="{{ '/contact/' | relative_url }}" class="btn btn-primary btn-lg">
      <i class="fas fa-paper-plane"></i> Enviar CV
    </a>
  </div>
</div>
