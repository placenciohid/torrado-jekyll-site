---
title: Galería
layout: page
description: Galería
---

Aquí puedes ver una selección de nuestros equipos.

<div class="row mt-5">
  {% assign equipment_images = site.static_files | where_exp: "item", "item.path contains 'assets/images/equipement'" %}
  {% for image in equipment_images %}
    <div class="col-md-4 mb-4">
      <a href="{{ image.path | relative_url }}" class="gallery-item">
        <div class="gallery-image-container">
          <img src="{{ image.path | relative_url }}" alt="{{ image.name | split: '.' | first }}" class="img-fluid rounded gallery-image">
        </div>
      </a>
    </div>
  {% endfor %}
</div>