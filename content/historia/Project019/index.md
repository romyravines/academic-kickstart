---
title: ¿Cuál es el volumen de productos que voy a distribuir?
summary: Venta Diaria y Mensual, por referencia y canal.
tags: ["Time Series", "Forecasting", "Statistics"]
categories: ["Distribution", "Demand"]

date: "2017-03-01T00:00:00Z"


image:
  caption: "Icons [Freepik](https://www.freepik.com/) from [Flaticon](https://www.flaticon.com/)"
  focal_point: "Smart"

---


## Pregunta de Negocio

Empresa distribuidora de bebidas. Requiere mejor la previsión de su distribución diaria y mensual a socios colaboradores ya que de eso depende directamente el cumplimiento del presupuesto anual.



## Objetivo

Un sistema predictivo para explicar y mejorar la previsión de su distribución, que permita evaluar y corregir las posibles desviaciones respecto al presupuesto anual y metas de negocio.



## Solución

 - Sistema de **modelación masiva**, necesario para prever las ventas a nivel de referencia y canal (miles de outputs), que garantiza la consistencia entre los resultados obtenido para el total de ventas y las ventas desagregadas.
 - **Modelo diario** de ventas. Sigue un calendario de lunes a viernes, filtrando festivos y proporcionando un trato especial los fines de mes, de trimestre y de año.
 - **Modelo mensual** de ventas. Realiza previsiones a tres niveles de desagregación: distribuidor, marca y referencia.
 - Este sistema **selecciona automáticamente la estructura ARIMA** e incluye elasticidades de parámetros externos como economía y temperatura.
 - El cliente visualiza las previsiones de manera remota en un **servicio web**.

