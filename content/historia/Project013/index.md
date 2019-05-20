---
title: ¿Cuántas personas ven mi anuncio?
summary: Anticipando el número de compradores que verán mi anuncio en TV.
tags: ["Machine Learning", "Forecasting"]
categories: ["Media"]

date: "2018-09-01T00:00:00Z"


image:
  caption: "Icons [Freepik](https://www.freepik.com/) from [Flaticon](https://www.flaticon.com/)"
  focal_point: "Smart"

---

## Pregunta de Negocio

Empresa del sector medios requiere estimar con alta precisión, los niveles de audiencia que tiene cada uno de los anuncios publicitarios que emite.


## Desafíos

 - Prever a 60 días vista, la audiencia por cadena de tv, franja horaria, bloque publicitario y público objetivo del producto/servicio publicitado.
 - Alto volumen de datos debido al nivel de desagregación en que se guardan los datos de audiencia. Por ejemplo, en 14 meses se archivan 7Gb.
  
  
## Solución

Se construye una solución con los siguientes módulos:

 - **Datamart analítico**. Integración de datos fuentes internas y externas (calendario, eventos deportivos, hechos que son noticia, etc.). Incluye la (re)construcción de indicadores de audiencia a diferentes niveles de desagregación.
 - **Modelos**. Módulo de modelos de machine learning (específicamente, gradient boosting machines) que incluye diagnosis exhaustiva de los resultados.
 - **Herramienta**. Visualización de datos, diagnosis de modelos y previsiones en informes dinámicos con actualización automática.
 
Esta solución se desarrolló íntegramente con SAS Viya.


## Resultados

 - En más del 70% de los bloques publicitarios, el MAE fue inferior a 1 unidad.
 - En más del 60% de los bloques publicitarios, el MAPE fue inferior al 20%
 - Sistema predictivo **escalable y reutilizable** en otros canales de tv y targets.
 - Sistema con **diagnosis exhaustiva** de resultados.
 - **Informes automáticos** de cada etapa del proceso de modelización e identificación del target.
 
 

<br> 
 
 {{< gallery >}} 
 
<br> 
