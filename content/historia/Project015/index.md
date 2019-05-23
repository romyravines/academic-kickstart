---
title: ¿Cuál será la aceptación de este nuevo producto tecnológico?
summary: Anticipando las ventas de un dispositivo completamente nuevo para el mercado.
tags: ["Statistics", "Forecasting", "Bayesian"]
categories: ["Telco", "Demand"]

date: "2014-09-01T00:00:00Z"


image:
  caption: "Icons [Freepik](https://www.freepik.com/) from [Flaticon](https://www.flaticon.com/)"
  focal_point: "Smart"

---

## Pregunta de Negocio

Empresa del sector de telecomunicaciones desea lanzar un nuevo tipo de reloj inteligente. Se trata de un producto nuevo para el mercado que no dispone de antecedentes similares.

## Objetivo 

Crear un Sistema de Previsión de Demanda de Nuevos Productos que apoye la toma de Decisiones de El Cliente sobre lanzamientos en los mercados donde está presente, antes inclusive de la definición de los detalles de comercialización
El Cliente quiere responder a: ​
 - ¿Lanzar o no Lanzar?​
 - ¿Cuál es la demanda al final del ciclo de vida?​
 - ¿Cuáles serán los beneficios que podemos obtener?​
 - ¿Qué semejanzas/diferencias hay entre países?​
 - ¿Cómo uso la información del Estudio de Mercado?​
 - ¿Qué recomendaciones sobre precio puedo dar?

## Desafíos

 - **Pocos datos**. Apenas un Estudio de Mercado (300 encuestas por mercado) e histórico corto de variables externas interesantes.
 - **Productos similares**. No existen muchos productos similares de donde aprender.
 - **Vida Muy Corta**. El producto puede perder vigencia rápidamente y/o verse afectado por el lanzamiento de productos similares de parte de la competencia
 - **Mercado Pequeño**. El público target es muy específico. Está altamente afectado por factores no controlables como las redes sociales.
 - **Estudio Mercado**. ¿Cómo utilizar los resultados del estudio de mercado en un sistema de modelación?

  
  
## Solución

La solución utilizó el enfoque teórico de la **Curva de Bass** (difusión tecnológica) y se ejecutó en dos fases:
 - Utilizar los coeficientes de Bass de la curva de un producto similar o de la curva media del mercado, y/o
 - Estimar los coeficientes de Bass a partir de indicadores macro y de telecom de cada mercado. 
La curvas de Bass de productos similares fueron ajustadas utilizando enfoque bayesiano. Los modelos utilizados para definir la curva de bass del producto a ser lanzado fueron dinámicos, jerárquicos y bayesianos.



## Resultados

- Al tratarse de un posible lanzamiento, no se pueden utilizar métricas de error de previsión.
- El resultado fue un simulador de Mercado Potencial a diferentes niveles de precio del producto y cuota mensual.


 

<br> 

 {{< gallery >}}  
 
<br> 
