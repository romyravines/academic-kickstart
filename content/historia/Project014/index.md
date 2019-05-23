---
title: ¿Cuántas horas-hombre necesito para mi próximo proyecto?
summary: Estimando el coste esperado del desarrollo de un nuevo proyecto.
tags: ["Machine Learning", "Forecasting"]
categories: ["Media"]

date: "2015-06-01T00:00:00Z"


image:
  caption: "Icons [Freepik](https://www.freepik.com/) from [Flaticon](https://www.flaticon.com/)"
  focal_point: "Smart"

---


## Pregunta de Negocio

Empresa del sector de tecnología informática requiere estimar correctamente el presupuesto real, medido en *horas-hombre*, 
de cada uno de sus proyectos en producción. La precisión de dicha estimación es un factor clave para que el Comité de Dirección
tome decisiones sobre oportunidades comerciales y planes a largo plazo.


## Objetivo

Desarrollar una herramienta para planear mejor sus recursos y tener un mayor control financiero de sus costes. La herramienta debe ayudar al dimensionamiento tanto en tiempo como en recursos de nuevos proyectos, así como el seguimiento de proyectos en activo.


## Desafíos

 - Tratamiento de los datos. No sólo la dificultad de manejar **diferentes formatos de datos**, sino también la **inconsistencia de la información** entre diferentes fuentes.
 - Definición de la unidad de análisis. No se utiliza la misma **definición de Proyecto** entre las diversas unidades de la organización
 - Tamaño de **muestra pequeña** y/o poco histórico para determinado tipo de proyectos. 
 - Información incompleta 
 
  
## Solución

El marco conceptual que se utilizó para formular la solución responde a la siguiente pregunta:
bajo un enfoque económico y de negocio ¿qué factores explican el esfuerzo necesario para desarrollar un proyecto?
Los factores se asociaron a los factores considerados clave para estimar el esfuerzo y el tiempo neceario y la variabilidad entre proyectos. Dichos factores son:
 - Escala o Tamaño del proyecto.
 - Nivel de Innovación.
 - Términos de la Negociación. 
 - Dinamica o Evolución del proyecto. 
 
El sistema final tiene +20 modelos organizados en 3 módulos: 
 1. **Esfuerzo Inicial**. Permite simular el número de horas-hombre que se requiere para desarrollar un proyecto, 
 con diferentes configuraciones.
 1. **Duración**. Permite estimar el número de semanas necesario para completar el 98% de un proyecto dado.
 1. **Seguimiento**. Permite actualizar el número de horas-hombre que se requiere para concluir los proyectos en desarrollo.
Los modelos utilizados son dinámicos y jerárquicos con enfoque bayesiano. Permiten trabajar con relaciones no lineales, utilizar la información de negocio de gerentes y dar 100% de explicatividad, con sentido de negocio, a los resultados.


## Resultados


 - **Estimación inicial del esfuerzo más precisa** que los dimensionamientos internos (cuando se considera la misma definición de esfuerzo de implementación). Mejora entre 20 y 40 pp cuando se utilizan los modelos predictivos.
 - Estimación **individual para cada proyecto** en producción y esfuerzo total, evitando el uso de segmentaciones previas (y por lo tanto de referencias propias).
 - Estimación de esfuerzo incluso para proyectos  aunque la **muestra histórica sea pequeña** o los proyectos se encuentren en curso.
 - Sistema para **actualizar las previsiones** de esfuerzo total **durante el desarrollo** del proyecto.
 - **Herramienta** de seguimiento del esfuerzo y tiempo ya gastados por mes y de las previsiones para los proyectos en curso.



<br> 
 
 {{< gallery >}} 
 
<br>

 

<br> 
 
 
<br> 