---
title: ¿Quién cancelará su suscripción?
summary: Anticipando la solicitud de baja de mis suscriptores
tags: ["Machine Learning", "Classification"]
categories: ["Clients", "Publishers"]

date: "2018-06-01T00:00:00Z"


image:
  caption: "Icons [Freepik](https://www.freepik.com/) from [Flaticon](https://www.flaticon.com/)"
  focal_point: "Smart"

---

## Pregunta de Negocio

Empresa del sector de prensa escrita requiere dirigir adecuadamente su esfuerzo en campañas para aumentar el éxito en la retención de sus suscriptores.

## Desafíos

  - Baja tasa de clientes que se dan de baja cada mes (menos de 1.0%).
  - Contexto de mercado muy difícil. La suscripción a prensa escrita está bajando constantemente. El mercado ofrece muchas alternativas y el contexto socio-económico condiciona mucho la actitud de los lectores frente a este tipo de medio.
  - Los beneficios adicionales que ofrece la suscripción dependen de terceros, que no facilitan los datos. Por lo tanto, no se puede identificar aquellos suscriptores que hacen real uso de beneficios adicionales.
  - La información disponible es de tipo cualitativo. Hay pocos indicadores cuantitativos que faciliten la estimación de la propensión.
  
  
## Solución

Se construye una solución con los siguientes módulos:

 - **Datamart analítico**. Integración de datos de diversas fuentes (datos del cliente, de la relación comercial, de su actividad, etc.)
 - **Feature engineering**. Procesos automáticos de preparación de datos para el algoritmo predictivo: *clustering*, *feature engineering* y *normalization*.
 - **Modelos**. Módulo de modelos de machine learning (específicamente, gradient boosting machines) que incluye selección de la mejor estrategia de modelización, incluye ensamblaje de modelos y diagnosis exhaustiva del modelo seleccionado. 
 - **Previsiones**. Procedimiento de puntuación (estimación de la propensión) a todos los clientes en dos niveles (cliente particular y suscripción)
 
Esta solución se desarrolló íntegramente con R. Se trabajó con información de varias decenas de miles de clientes.


## Resultados

 - **Acierto** del 80% en la identificación de bajas a un mes vista.
 - Sistema predictivo **escalable y reutilizable** en otros segmentos de clientes.
 - Sistema con **diagnosis exhaustiva** de resultados.
 - **Informes automáticos** de cada etapa del proceso de modelización e identificación del target.
 