---
title: Marcas
layout: modern-page
description: "Representamos las mejores marcas de maquinaria agrícola: Case IH, New Holland, Kubota y más. Equipos de calidad con soporte técnico en Puerto Rico."
---

<div style="text-align: center; max-width: 800px; margin: 0 auto var(--space-12);">
  <span class="section-label">Nuestras Marcas</span>
  <h2 style="margin-bottom: var(--space-4);">Equipos de Confianza para Tu Operación Agrícola</h2>
  <p style="font-size: 1.125rem; color: var(--color-text-light);">
    En <strong>Torrado Equipment</strong> representamos exclusivamente las <strong>mejores marcas</strong> 
    del mercado agrícola mundial. Cada fabricante ha sido seleccionado por su trayectoria comprobada, 
    innovación tecnológica y compromiso con la durabilidad.
  </p>
</div>

<div class="brands-showcase">
  {% assign brand_images = site.static_files | where_exp: "item", "item.path contains 'assets/images/brands'" %}
  {% for brand_image in brand_images %}
    {% assign brand_name = brand_image.name | split: '.' | first %}
    {% assign clean_name = brand_name | replace: '-', ' ' | replace: '_', ' ' | replace: 'logo', '' | replace: 'copy', '' | replace: 'images', '' | replace: '(', '' | replace: ')', '' | replace: '1', '' | replace: '2', '' | replace: '3', '' | replace: '4', '' | replace: '5', '' | replace: '__', '' %}
    <div class="brand-card animate-on-scroll">
      <div class="brand-card-logo">
        <img alt="{{ clean_name }}" src="{{ brand_image.path | relative_url }}" loading="lazy" />
      </div>
      <span class="brand-card-name">{{ clean_name }}</span>
    </div>
  {% endfor %}
</div>

<div style="background: linear-gradient(135deg, var(--color-gray-50), var(--color-white)); border-radius: var(--radius-2xl); padding: var(--space-12); margin-top: var(--space-16); border: 1px solid var(--color-border);">
  <h3 style="text-align: center; margin-bottom: var(--space-8);">¿Por qué elegir nuestros equipos?</h3>
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: var(--space-6);">
    <div style="display: flex; align-items: flex-start; gap: var(--space-4);">
      <div style="width: 48px; height: 48px; background: linear-gradient(135deg, var(--color-primary), var(--color-primary-light)); border-radius: var(--radius-lg); display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
        <i class="fas fa-award" style="color: white;"></i>
      </div>
      <div>
        <h4 style="margin-bottom: var(--space-2);">Calidad Garantizada</h4>
        <p style="color: var(--color-text-light); margin: 0;">Respaldada por décadas de experiencia</p>
      </div>
    </div>
    <div style="display: flex; align-items: flex-start; gap: var(--space-4);">
      <div style="width: 48px; height: 48px; background: linear-gradient(135deg, var(--color-primary), var(--color-primary-light)); border-radius: var(--radius-lg); display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
        <i class="fas fa-microchip" style="color: white;"></i>
      </div>
      <div>
        <h4 style="margin-bottom: var(--space-2);">Tecnología Avanzada</h4>
        <p style="color: var(--color-text-light); margin: 0;">Máxima eficiencia operativa</p>
      </div>
    </div>
    <div style="display: flex; align-items: flex-start; gap: var(--space-4);">
      <div style="width: 48px; height: 48px; background: linear-gradient(135deg, var(--color-primary), var(--color-primary-light)); border-radius: var(--radius-lg); display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
        <i class="fas fa-headset" style="color: white;"></i>
      </div>
      <div>
        <h4 style="margin-bottom: var(--space-2);">Soporte Técnico</h4>
        <p style="color: var(--color-text-light); margin: 0;">Disponibilidad de repuestos</p>
      </div>
    </div>
    <div style="display: flex; align-items: flex-start; gap: var(--space-4);">
      <div style="width: 48px; height: 48px; background: linear-gradient(135deg, var(--color-primary), var(--color-primary-light)); border-radius: var(--radius-lg); display: flex; align-items: center; justify-content: center; flex-shrink: 0;">
        <i class="fas fa-chart-line" style="color: white;"></i>
      </div>
      <div>
        <h4 style="margin-bottom: var(--space-2);">Valor de Reventa</h4>
        <p style="color: var(--color-text-light); margin: 0;">Protege tu inversión</p>
      </div>
    </div>
  </div>
</div>

<div style="text-align: center; margin-top: var(--space-12);">
  <p style="font-size: 1.25rem; color: var(--color-primary); font-weight: 600;">
    <i class="fas fa-quote-left" style="color: var(--color-accent); margin-right: var(--space-2);"></i>
    Invierte en equipos que trabajan tan duro como tú.
    <i class="fas fa-quote-right" style="color: var(--color-accent); margin-left: var(--space-2);"></i>
  </p>
</div>
