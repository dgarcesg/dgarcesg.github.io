---
layout: page
title: Monitor de incendios forestales con satélites y clima
description: ¿Qué incendios podían crecer en la semana del 22 al 28 de octubre de 2026?
img: assets/img/incendios_pronostico.png
img_alt: Mapa de calor con el riesgo pronosticado por día en cinco distritos del Perú
importance: 3
pregunta: ¿Qué incendios podían crecer en la semana del 22 al 28 de octubre de 2026?
resultado: "Río Tambo: 2 días de riesgo y 19 mm de lluvia, frente a 55–72 mm en los distritos de Ucayali."
enlaces:
  - nombre: Código
    url: https://github.com/dgarcesg/monitor-de-incendios
  - nombre: Notebook
    url: https://github.com/dgarcesg/monitor-de-incendios/blob/main/Tarea_Raster.ipynb
---

Los focos de calor dicen dónde arde hoy. Este monitor, hecho con datos al 21 de octubre de 2026, buscó dónde podía arder más en los 7 días siguientes, en los 5 distritos más afectados del Perú.

Para no inventar umbrales, comparé el pronóstico con el clima de los días en que más ardió cada distrito la semana anterior.

<img src="{{ '/assets/gif/evolucion_top5.gif' | relative_url }}" class="img-fluid rounded z-depth-1" width="100%" height="auto" alt="Animación de los focos de calor en los 5 distritos más afectados, del 14 al 21 de octubre de 2026" loading="lazy">

## Qué encontré

<div class="my-3">
  {% include figure.liquid path="assets/img/incendios_pronostico.png" class="img-fluid rounded z-depth-1" alt="Mapa de calor con el riesgo pronosticado por día en cinco distritos del Perú" caption="Riesgo pronosticado por distrito. El recuadro negro marca los días de riesgo." %}
</div>

- **La lluvia del 17 de octubre cortó el pico de la semana.** En el Perú hubo 6986 focos del 14 al 16 de octubre, frente a 2963 en los cinco días siguientes.
- **Río Tambo era el incendio con más posibilidad de crecer.** Fue el único distrito con dos días de riesgo y el que menos lluvia esperaba. Nueva Requena, el de mayor huella, no tuvo ninguno.
- **La huella satelital infla el área.** El incendio principal de Nueva Requena quemó 166 ha según Sentinel-2, frente a las 412 ha de su huella VIIRS: 2,5 veces más.

<div class="my-3">
  {% include figure.liquid path="assets/img/incendios_dnbr.jpg" class="img-fluid rounded z-depth-1" alt="Imágenes Sentinel-2 antes y después del incendio de Nueva Requena, con el área quemada" caption="Incendio de Nueva Requena antes y después, según Sentinel-2." %}
</div>

## Cómo leer estas cifras

- Es un pronóstico de octubre de 2026 y no lo contrasté con lo que ocurrió después. «Puede crecer» no es «va a crecer».
- La calibración es corta: 8 días y 5 distritos.
- Las nubes esconden el fuego, y no todo incendio deja un foco de calor.

Es una herramienta independiente con fines académicos: no reemplaza los reportes del COEN, INDECI, SERFOR ni SERNANP.
