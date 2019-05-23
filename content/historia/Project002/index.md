---
title: ¿Qué opina El Cliente?
summary: Analítica de Textos para entender el feedback de los Clientes.
tags: ["Machine Learning", "Text Mining", "Marketing","Clients"]
categories: ["Utilities", "Clients"]

date: "2018-09-01T00:00:00Z"

image:
  caption: "Icons [Freepik](https://www.freepik.com/) from [Flaticon](https://www.flaticon.com/)"
  focal_point: "Smart"
---


## Pregunta

¿Qué temas son los más relevantes para los clientes de mi sector, teniendo en cuenta los comentarios que realizan en la Encuesta de Satisfacción que realizo cada año?



## Solución

Utilizado +5k comentarios realizados a lo largo de 12 meses, se construye un sistema de clasificación automática basado en algoritmos de **text analytics**. En particular, se aplica SVD+Varimax para la identificación de temas (*topic modelling*). y se construye un modelo supervisado para conocer el sentimiento del comentario (*sentimental analysis*).



## Resultado

 - Coincidencia del 94% de la identificación automática de temas con los puntos de contacto del customer journey identificado manualmente.
 
 - Estimación de la importancia del peso de cada tema para cada cliente encuestado. No se pierde la visión cliente en el proceso de etiquetado de comentarios.  
 
 - Reorganización y disminución del número de etiquetas (temas) para clasificar comentarios.
 
 - Acierto del 95% en el reconocimiento del sentimiento.

 - Reducción del tiempo de atención a clientes debido a la sustitución de la clasificación manual con la clasificación automática.
