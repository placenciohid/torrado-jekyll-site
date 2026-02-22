---
title: Galería
layout: modern-page
description: "Galería de equipos agrícolas disponibles en Torrado Equipment. Tractores, implementos y maquinaria para tu operación en Puerto Rico."
glightbox: true
---

<div style="text-align: center; max-width: 800px; margin: 0 auto var(--space-12);">
  <span class="section-label">Nuestros Equipos</span>
  <h2 style="margin-bottom: var(--space-4);">Galería de Maquinaria Agrícola</h2>
  <p style="font-size: 1.125rem; color: var(--color-text-light);">
    Explora nuestra selección de equipos de alta calidad. Haz clic en cualquier imagen 
    para verla en tamaño completo y descubre las máquinas que pueden transformar tu operación agrícola.
  </p>
</div>

<div class="gallery-masonry">
  {% assign equipment_images = site.static_files | where_exp: "item", "item.path contains 'assets/images/equipement'" %}
  {% for image in equipment_images %}
    <a href="{{ image.path | relative_url }}" class="glightbox gallery-item" data-gallery="equipment">
      <div class="gallery-image-container">
        <img src="{{ image.path | relative_url }}" alt="{{ image.name | split: '.' | first | replace: '-', ' ' | replace: '_', ' ' }}" loading="lazy">
      </div>
    </a>
  {% endfor %}
</div>

