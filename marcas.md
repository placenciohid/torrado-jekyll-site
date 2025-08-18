---
title: Marcas
layout: page
description: Marcas
---

## Equipos de Confianza para Tu Operación Agrícola

En **Torrado Equipment** representamos exclusivamente las **mejores marcas** del mercado agrícola mundial. Cada fabricante ha sido seleccionado por su **trayectoria comprobada**, innovación tecnológica y compromiso con la durabilidad.

### ¿Por qué elegir nuestros equipos?

- **Calidad garantizada** respaldada por décadas de experiencia
- **Tecnología avanzada** para máxima eficiencia operativa
- **Soporte técnico especializado** y disponibilidad de repuestos
- **Valor de reventa superior** que protege tu inversión

**Invierte en equipos que trabajan tan duro como tú.**

<div class="row justify-content-center mt-5">
  {% assign brand_images = site.static_files | where_exp: "item", "item.path contains 'assets/images/brands'" %}
  {% for brand_image in brand_images %}
    <div class="col-6 col-md-4 col-lg-3 mb-4 d-flex justify-content-center align-items-center">
      <div class="brand-logo">
        <img alt="{{ brand_image.name | split: '.' | first }}" src="{{ brand_image.path | relative_url }}" />
      </div>
    </div>
  {% endfor %}
</div>