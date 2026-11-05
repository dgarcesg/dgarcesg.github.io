---
layout: page
title: Servidor MCP que conecta a Claude con las cifras oficiales del BCRP
description: ¿Acierta Claude cifras oficiales del BCRP con y sin acceso a los datos?
img: assets/img/mcp_grafico.png
img_alt: Gráfico de barras con 10 respuestas «no sé» sin herramientas y 10 aciertos con el servidor
importance: 2
pregunta: ¿Acierta Claude cifras oficiales del BCRP con y sin acceso a los datos?
resultado: 10 de 10 aciertos con el servidor; sin él, 10 «no sé».
enlaces:
  - nombre: Código
    url: https://github.com/dgarcesg/MCP-BCRP
  - nombre: Informe
    url: https://github.com/dgarcesg/MCP-BCRP/blob/main/informe.md
---

Construí un servidor MCP que le da a Claude acceso a las 17 mil series estadísticas del Banco Central de Reserva del Perú: busca la serie, descarga los datos, hace las cuentas en Python y cita la fuente.

## Qué medí

Le hice a Claude Haiku 10 preguntas sobre cifras oficiales, como la inflación, el tipo de cambio o las reservas internacionales, de dos maneras: sin herramientas y con el servidor. Cada respuesta se comparó con la cifra oficial.

<div class="my-3">
  {% include figure.liquid path="assets/img/mcp_grafico.png" class="img-fluid rounded z-depth-1" alt="Gráfico de barras con 10 respuestas «no sé» sin herramientas y 10 aciertos con el servidor" caption="Resultados de las 10 preguntas en cada modo." %}
</div>

## Qué encontré

- **Con el servidor acertó las 10**, cada una con el código de la serie, el periodo y la URL de la fuente.
- **Sin herramientas no inventó cifras:** respondió «no sé» en las 10.
- **El costo es el tiempo:** 31,6 segundos por pregunta con el servidor, frente a 11,6 sin él.

## Cómo leer estas cifras

- Es una sola corrida con un solo modelo, así que el resultado puede variar.
- La instrucción pedía no estimar. Por eso este experimento no dice si, sin esa instrucción, el modelo habría inventado cifras.
