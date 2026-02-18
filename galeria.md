---
title: Galería
layout: modern-page
description: "Galería de equipos agrícolas disponibles en Torrado Equipment. Tractores, implementos y maquinaria para tu operación en Puerto Rico."
glightbox: true
---

Aquí puedes ver una selección de nuestros equipos. Haz clic en cualquier imagen para verla en tamaño completo.

<div class="gallery-masonry mt-5">
  {% assign equipment_images = site.static_files | where_exp: "item", "item.path contains 'assets/images/equipement'" %}
  {% for image in equipment_images %}
    <a href="{{ image.path | relative_url }}" class="glightbox gallery-item" data-gallery="equipment">
      <div class="gallery-image-container">
        <img src="{{ image.path | relative_url }}" alt="{{ image.name | split: '.' | first }}" class="gallery-image" loading="lazy">
      </div>
    </a>
  {% endfor %}
</div>
