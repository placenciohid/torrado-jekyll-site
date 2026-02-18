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

<div style="background: linear-gradient(135deg, var(--color-primary), var(--color-primary-light)); border-radius: var(--radius-2xl); padding: var(--space-12); margin-top: var(--space-16); color: var(--color-white); text-align: center;">
  <h3 style="color: var(--color-white); margin-bottom: var(--space-4);">¿Te interesa algún equipo?</h3>
  <p style="opacity: 0.9; max-width: 600px; margin: 0 auto var(--space-8);">
    Contáctanos para conocer disponibilidad, precios y opciones de financiamiento. 
    Nuestros especialistas te ayudarán a encontrar la máquina perfecta para tu operación.
  </p>
  <div style="display: flex; gap: var(--space-4); justify-content: center; flex-wrap: wrap;">
    <a href="{{ '/contact/' | relative_url }}" class="btn btn-primary btn-lg" style="background: var(--color-accent); color: var(--color-gray-900);">
      <i class="fas fa-envelope"></i> Solicitar Información
    </a>
    <a href="{{ '/services/ventas/' | relative_url }}" class="btn btn-outline btn-lg" style="border-color: white; color: white;">
      <i class="fas fa-tractor"></i> Ver Servicios de Venta
    </a>
  </div>
</div>
