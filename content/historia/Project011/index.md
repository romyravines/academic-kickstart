---
title: ¿A quién debo retener?
summary: Identificando a los clientes más propensos a la fuga
tags: ["Machine Learning", "Classification"]
categories: ["Clients", "Utilities"]

date: "2018-12-01T00:00:00Z"

# Set captions for image gallery.
gallery_item:
- album: gallery
  caption: #ML
  image: Imagen1.png
- album: gallery
  caption: #ML
  image: Imagen2.png
- album: gallery
  caption: #ML
  image: Imagen3.png
- album: gallery
  caption: #ML
  image: Imagen4.png
- album: gallery
  caption: #ML
  image: Imagen5.png
- album: gallery
  caption: #ML
  image: Imagen6.png


image:
  caption: "Icons [Freepik](https://www.freepik.com/) from [Flaticon](https://www.flaticon.com/)"
  focal_point: "Smart"

---



## Pregunta de Negocio

Empresa del sector de energía va a aumentar su presupuesto en acciones de retención, por lo que requiere dirigir sus camapañas a un público seleccionado cuidadosamente.



## Desafíos

  - Baja tasa de clientes que se dan de baja cada mes (menos de 0.5%).
  - Debido a los procesos de actualización de datos en los sistemas internos, la propensión a la baja debe estimarse con al menos dos meses de anticipación. 
  - Los datos de la competencia no están disponibles.
  - Cambios en la legislación del sector han provocado cambio en el comportamiento de clientes respecto al churn, dejando poco histórico de la nueva situación.
  


  
## Solución

Se construye una solución end-to-end con los siguientes módulos:

 - **Datamart analítico**. Procedimientos desatentidos de actualización del conjunto de datos.
 - **Feature engineering**. Procesos automáticos de preparación de datos para el algoritmo predictivo: *clustering*, *feature engineering* y *normalization*.
 - **Modelos**. Módulo de modelos de machine learning (específicamente, gradient boosting machines) que incluye selección de estrategia de modelización, control de calidad con backtesting y diagnosis exhaustiva del modelo seleccionado. 
 - **Previsiones**. Procedimiento de puntuación (estimación de la propensión) a todos los clientes. Selección del Top indicado por el usuario final, teniendo en consideración criterios de negocio adicionales. Incluye matriz de interpretabilidad de resultados.
 
 
Esta solución se desarrolló íntegramente con R. Se trabajó con información de varios cientos de miles de clientes. El entorno de desarrollo se encontraba en AWS.



## Resultados

 - Actualización **desatendida** de base de datos y optimización del tiempo para tratamiento de datos de 2 horas a 15 minutos.
 - Sistema con **+1200 indicadores** construidos y **+100 modelos** compitiendo.
 - Sistema con **diagnosis exhaustiva** de resultados.
 - **Informes automáticos** de cada etapa del proceso de modelización e identificación del target.
 - **Mejora del lift** de 2.0 a 5.5.
 - Sistema predictivo **escalable y reutilizable** en otros segmentos de clientes.

<br> 
 
 {{< gallery >}} 
 
<br> 
 