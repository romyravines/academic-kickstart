---
title: ¿Cuántas cajas de cada medicina me van a solicitar?
summary: Demanda de Medicinas por Cuenta
tags: ["Machine Learning", "Demand", "Forecasting", "Health"]
categories: ["Health", "Demand"]

date: "2019-02-01T00:00:00Z"


image:
  caption: "Icons [Freepik](https://www.freepik.com/) from [Flaticon](https://www.flaticon.com/)"
  focal_point: "Smart"

---

## Pregunta de Negocio

Empresa farmacéutica requiere conocer la demanda de un determinado medicamento, por cuenta, con 6 meses de anticipación.


## Desafíos

  - **Pocos datos históricos** ya que se trata de un producto con apenas 18 meses en el mercado. Varias cuentas tienen apenas 3 pedidos en ese periodo.
  - **Demanda intermitente**. Los pedidos no se realizan todos los dias/semanas. Las series temporales tienen muchos ceros (semanas sin pedidos).
  - No se dispone de la demanda potencial. Los datos sobre el **número de pacientes** que atiende cada cuenta no están disponiblen.
  - Poca información de drivers. La acción comercial y actividades de marketing no están 100% alineadas o vinculadas con una cuenta y/o medicina.
  
  
## Solución

Se construye una solución end-to-end con los siguientes módulos:

 - Datamart analítico. Conjunto de datos tratados que vinculan varias fuentes de información. Incluye procesos de normalización de datos y recuperación de información a nivel cuenta/cliente.
 - Patrones de compra. Módulo de identificación y caracterización de los patrones de compra trimestral de cada cuenta. Se identifican hasta 7 patrones diferentes, según la curva de "stock".
 - Previsiones de compra. Módulo de modelos de machine learning (gradient boosting machines) que estima modelos y proporciona previsiones de cada cuenta.
 - Herramienta. Módulo con informes que permiten interactuar con el datamart, los patrones de compra y las previsiones a nivel cuenta y en agregaciones predefinidas por el usuario final.


## Resultados

 - Sistema con previsiones para los siguientes 6 meses, a diferentes niveles de agregación territorial.
 - Previsiones para todas las cuentas, incluidas aquellas con muy poco histórico.
 - Datos de actividad comercial y venta vinculados y organizados, incluyendo nuevos KPIs.
 - Previsiones explicadas ya que el sistema utiliza métodos de interpretabilidad de resultados de algoritmos de machine lerarning.
 - Herramienta de visualización de datos y previsiones.
