---
title: Marcas
layout: page
description: "Representamos las mejores marcas de maquinaria agrícola: Case IH, New Holland, Kubota y más. Equipos de calidad con soporte técnico en Puerto Rico."
---

## Equipos de Confianza para Tu Operación Agrícola

En **Torrado Equipment** representamos exclusivamente las **mejores marcas** del mercado agrícola mundial. Cada fabricante ha sido seleccionado por su **trayectoria comprobada**, innovación tecnológica y compromiso con la durabilidad.

### ¿Por qué elegir nuestros equipos?

- **Calidad garantizada** respaldada por décadas de experiencia
- **Tecnología avanzada** para máxima eficiencia operativa
- **Soporte técnico especializado** y disponibilidad de repuestos
- **Valor de reventa superior** que protege tu inversión

**Invierte en equipos que trabajan tan duro como tú.**

<div class="brands-showcase mt-5">
  {% assign brand_images = site.static_files | where_exp: "item", "item.path contains 'assets/images/brands'" %}
  {% for brand_image in brand_images %}
    <div class="brand-card animate-on-scroll">
      <div class="brand-card-logo">
        <img alt="{{ brand_image.name | split: '.' | first }}" src="{{ brand_image.path | relative_url }}" loading="lazy" />
      </div>
      <span class="brand-card-name">{{ brand_image.name | split: '.' | first }}</span>
    </div>
  {% endfor %}
</div>
