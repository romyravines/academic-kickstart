---
title: Desestacionalización de Series de Tiempo Económicas
summary: Naturaleza de las fluctuaciones de los datos económicos.
tags: ["Others"]
categories: ["Others"]

date: "2009-05-01T00:00:00Z"

image:
  caption: ""
  focal_point: ""
---

"Desestacionalización de Series de Tiempo Económicas: Metodología y Aplicación a los Indicadores de Producción y Precios" es el último de los tres títulos en los cuales trabajé como asistente de investigación. bajo la dirección del Econ. Marcos Robles. Fue publicado por el INEI en 1996.

En la publicación se describen las razones, las causas y la naturaleza de las fluctuaciones estacionales de las series de tiempo económicas y se evalúan algunos métodos de ajuste estacional, con el propósito de determinar el más adecuado y luego aplicarlo a series de producción y precios.

Por lo menos existen cuatro *causas*, no necesariamente excluyentes, que generan la estacionalidad:

 - las fechas fijadas institucionalmente para realizar ciertas actividades a lo largo del año;
 - el clima o las estaciones del año;
 - las expectativas respecto a las fluctuaciones estacionales y
 - el efecto del número de días hábiles y calendario dentro de un periodo.

Las *características* más importantes de las fluctuaciones estacionales son las siguientes:

 - se repiten cada año con una regularidad más o menos definida,
 - pueden medirse y separarse de las otras fuerzas que influyen en el comportamiento de la serie y
 - son causadas principalmente por fuerzas extraeconómicas.

Las *razones* más importantes para aplicar la desestacionalización de series son:

 - tener una apreciación más clara sobre su comportamiento debido exclusivamente a razones de tipo económico,
 - facilitar la identificación de patrones de comportamiento subyacentes en las series,
 - ayudar a conocer cómo se relacionan las series de interés con otras series (eventos exógenos o variables de política),
 - ayudar a disminuir las posibilidades de ser engañados por correlaciones de ”casualidad” entre series que pueden generarse por influencias estacionales sistemáticas e independientes.

Los *modelos básicos de descomposición* de series son: el aditivo, multiplicativo y aditivo logarítmico. A partir de estos modelos el problema de la desestacionalización consiste en estimar los componentes para cada uno de los periodos de observación.

Los *métodos de ajuste estacional* revisados en el trabajo se refieren a los métodos de regresión, métodos que emplean modelos ARIMA y los métodos de promedios móviles (el método simple y el X11-ARIMA).

La elección del método más apropiado dependerá del objeto de la desestacionalización:

 - se usará uno de tipo econométrico si lo que se busca es utilizar las series ajustadas estacionalmente como insumo de una análisis de regresión,
 - se usará uno que combina los aspectos deterministas de los métodos de regresión con los aspectos dinámicos de los métodos de promedios móviles (por ejemplo, algún componente con regresiones y los otros con promedios móviles) si lo que se busca es el análisis detallado y el pronóstico de una serie específica,
- se usará el de los promedios móviles si lo que se pretende es tener una apreciación de la tendencia de la serie, sin el componente estacional que la pueda oscurecer,o simplemente presentar las series desestacionalizadas de manera frecuente y masiva.

Una consideración adicional abona en favor de la utilización de métodos como el X11-ARIMA o el de modelos ARIMA: el hecho de que los modelos de regresión tienen el supuesto implícito de estabilidad de los parámetros y por ende la de los factores estacionales, al igual que el método que usa de manera simple los promedios móviles, los cuales en la práctica solo se satisfacen en ocasiones muy raras. El X11-ARIMA es, además, uno de los métodos más conocidos y utilizados para desestacionalizar series en las instituciones de estadística en el mundo.

Para elegir el modelo más adecuado, entre el aditivo (incluido el logarítmico) y el multiplicativo, debería tenerse en consideración lo siguiente: elegir el aditivo si se observa que el componente estacional es constante en el tiempo y el multiplicativo si es creciente o decreciente en el tiempo. Sin embargo, dependiendo de la información de la serie, la elección puede estar en muchos casos predeterminado. Un modelo multiplicativo no podría emplearse para una serie que contenga valores ceros o negativos, al igual que uno logarítmico no podría utilizarse si la serie contiene cifras negativas.

En el trabajo se aplican cuatro métodos de desestacionalización a la serie Indice del *PBI global* (con base 1979=100) correspondiente al periodo enero de 1983 - febrero de 1996: el econométrico de variables dicotómicas, el de modelos ARIMA,el más simple de promedios móviles y el X11-ARIMA.

Al final se eligió este último para desestacionalizar a un conjunto más amplio de series debido a las siguientes razones:

 - presenta la menor suma de cuadrados de los coeficientes de variación para diferentes
 - tamaños de muestra, es decir, este método proporciona estimaciones del factor estacional más estables en relación a los otros métodos,
 - da un tratamiento adecuado a los valores extremos de la serie, impidiendo caer en sesgos de las estimaciones del componente estacional,
amplía la información hacia atrás y hacia adelante mediante la construcción de modelos ARIMA, evitando con ello la pérdida de información que inevitablemente se produce cuando la información es filtrada con promedios móviles,
existen paquetes estadísticos que efectúan la desestacionalización con el X11-ARIMA de manera masiva y rutinaria, a diferencia, por ejemplo, del econométrico o el que utiliza los modelos ARIMA que requieren de todo un proceso para la construcción de los modelos.

En el trabajo se estimaron los componentes de tendencia y estacionalidad de dos conjuntos de indicadores: de producción y precios. Como se sabe el primero de ellos contiene series que en general presentan en su evolución una mayor influencia de los factores estacionales (el clima, el número de días hábiles, fechas especiales fijadas institucionalmente, las expectativas, etc.), mientras que el segundo conjunto, si bien muestran un comportamiento estacional mediatizado por la fuerza del componente irregular, es el que quizá captura más la atención de los agentes económicos debido a que el comportamiento de las series involucradas reflejan la evolución de la inflación del país y por ende los efectos sobre la capacidad adquisitiva de la población.

La estimación para los indicadores de producción se hizo con series mensuales, mientras que para los precios con series trimestrales, siendo, en ambos casos, la fuente utilizada el Sistema de Información Económico Mensual (SIEM) del [INEI](www.inei.gob.pe/).

[Ver Libro Digital en el site del INEI](http://proyectos.inei.gob.pe/web/biblioineipub/bancopub/Est/Lib0094/Libro.htm)

