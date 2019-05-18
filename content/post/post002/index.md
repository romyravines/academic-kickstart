---
title: '¿Supervisado o No?'
subtitle: '¿Qué enfoque de analytics debo usar?'
summary: Breve definición de los tipos de problemas a los que nos enfrentamos y los enfoques que se aplican en cada caso.
authors:
- admin
tags: ["Historia","Machine Learning", "Statistics"]
categories: ["Machine Learning"]
date: "2017-04-01T00:00:00Z"
lastmod: "2017-04-01T00:00:00Z"
featured: false
draft: false

# Featured image
image:
  caption: ''
  focal_point: ""
  preview_only: false

# Projects (optional).
projects: []


---

# ¿Supervisado o No?


<img src='/post/post002/mlalgorithms01.png' alt="" style="float:width:90%;">



En bastante común que los algoritmos de *Machine Learning* en
aprendizaje supervisado y aprendizaje no supervisado. Esta misma
clasificación se menciona en la sección @ref(clasemodelos), las
herramientas de *statistical learning*. Este tipo de clasificación
responde al tipo de problema e información que disponemos del *output*,
por ello, en este Manual generalizamos esta clasificación y la
denominamos **Tipo de Problema Analítico** que debemos afrontar.

<br>

**Problema / Aprendizaje Supervisado**

En el **aprendizaje supervisado**, cada dato, unidad analizada u
observación está etiquetada o asociada con una categoría o valor de
interés. Ejemplos:

-   Una imagen es etiquetada como un ‘gato’ o ‘perro’.
-   Un cliente es etiquetado como ‘propenso’ o ‘no propenso’ al uso del
    canal digital.
-   El precio de venta asociado a un coche usado, es una etiqueta de
    valor.

El objetivo del aprendizaje supervisado es estudiar muchos ejemplos
etiquetados y, luego, poder realizar predicciones sobre los datos
futuros. Por ejemplo, identificar nuevas fotografías con el animal
correcto, identificar clientes a clientes facilitar el uso de la banca
online o asignar precios de venta precisos a otros coches usados.

El aprendizaje supervisado usa técnicas de **clasificación** y
**regresión** para desarrollar modelos predictivos.

-   Las técnicas de **clasificación** predicen **respuestas discretas**
    —por ejemplo, saber si un correo es genuino o *spam*, o si un tumor
    es benigno o maligno. Los modelos de clasificación categorizan los
    datos de entrada. Entre las aplicaciones típicas se incluyen
    imágenes médicas, reconocimiento de voz o puntaje crediticio. Cuando
    hay sólo dos opciones, se denomina clasificación de dos clases o
    binaria. Cundo hay más categorías, se denomina clasificación
    multiclase o multinomial.

    -   En algunos casos la **detección de anomalías** se considera una
        técnica adicional de clasificación. En la detección de fraude,
        por ejemplo, los patrones de gasto de tarjeta de crédito muy
        poco habituales son sospechosos. Las posibles variaciones son
        tan numerosas y los ejemplos de formación son tan pocos, que no
        es posible saber de qué actividad fraudulenta se trata. El
        enfoque que toma la detección de anomalías es simplemente
        aprender qué puede considerarse como actividad normal (haciendo
        uso de las transacciones no fraudulentas del historial) e
        identificar todo lo que sea significativamente diferente[1].

-   Las técnicas de **reducción de dimensionalidad ** ayudan a disminuir
    la complejidad de los problemas debida al gran volumen de datos.
    Cuando mayor es el conjunto de datos, mayor la necesidad de reducir
    el número de variables (*features*) que se quieren analizar.

-   Las técnicas de **regresión** predicen **respuestas continuas** —por
    ejemplo, cambios en la temperatura o fluctuaciones en la demanda de
    energía. Las aplicaciones típicas pueden ser previsión del recurso
    eléctrico o trading algorítmico.

<br>

**Problema / Aprendizaje No Supervisado**

En el **aprendizaje no supervisado**, los datos no tienen etiquetas
asociadas a ellos. En este caso, el objetivo es organizar los datos de
alguna manera o describir su estructura. Esto puede significar agrupar
clientes en segmentos, o buscar diferentes maneras de examinar datos
complejos para que parezcan más simples.

El aprendizaje no supervisado se utiliza en análisis exploratorio de
datos para encontrar características ocultas y agrupar. Las aplicaciones
del clustering incluyen análisis de secuencias genéticas, investigación
de mercado y reconocimiento de objetos.


Enfoques de Modelización
------------------------

*Statistical Learning* se refiere a un conjunto de herramientas para
modelar y comprender conjuntos de datos complejos.

<br>

*Statistical Learning* es un término presentado en @isl2014. Hace
referencia a un área de reciente desarrollo en estadística, que se
combina con desarrollos paralelos de ciencias de la computación
(específicamente, *Machine Learning*). Se refiere a un ámplio conjunto
de herramientas para **entender datos**. Estas herramientas pueden ser:
**supervisadas** o **no supervisadas**. De manera muy genérica, en los
problemas supervisados se busca estimar o prever un *output* basado en
uno o más *inputs*. En los problemas no supervisados, se cuenta con los
*inputs* pero con un *output*, por lo que se busca entender la
estructura de los datos.

Otra forma de clasificar los métodos para modelizar se basa en su
objetivo y forma de construcción. Cuando se prioriza la **interpretación
del modelo**, buscando que expliquen las relaciones entre *output* e
*inputs*, se habla de **modelos estadísticos**. Cuando se prioriza la
**precisión de la previsión** se habla de algoritmos de **machine
learning**.

Tipos de modelos analíticos: *Modelos Estadísticos* y *Machine
Learning*[2]. Los primeros hacen uso de la probabilidad (inferencia),
son explicativos y predictivos. Los segundos suelen ser ‘cajas negras’,
se centran en la previsión y el trabajo con grandes volúmenes de
datos[3].

<br>

<img src='https://www.edvancer.in/wp-content/uploads/2016/01/ML-vs.-stats1.png' alt="Model" style="float:width:90%;">

<br>

El objetivo de los modelos o algoritmos de **Machine Learning** es
enseñar a las computadoras a hacer lo que es natural para humanos y
animales: **aprender de la experiencia**. Estos algoritmos utilizan
métodos computacionales para “aprender” información directamente de los
datos, sin depender de una ecuación predeterminada como modelo. Los
algoritmos mejoran su rendimientode forma adaptativa conforme aumenta la
cantidad de muestras (datos) disponibles para el aprendizaje.

<br>

**Machine Learning**

El *Machine Learning* no requiere hipótesis previas sobre las relaciones
subyacentes entre las variables (o inputs). Sólo se deben ingresar todos
los datos que se diponga, y el algoritmo procesa los datos y descubre
patrones, con los cuales puede hacer predicciones sobre el nuevo
conjunto de datos. El aprendizaje automático trata un algoritmo como una
**black box** (caja negra), siempre que funcione. En otras palabras, su
principal objetivo es la previsión.

<br>

**Modelos Estadísticos**

Por el contrario, los **estadísticos** deben comprender cómo se
recopilaron los datos, las propiedades estadísticas de los estimadores,
la distribución subyacente de la población que están estudiando y los
tipos de propiedades que esperaría si hiciera el experimento muchas
veces. Necesita saber exactamente lo que está haciendo y proponer
parámetros que le proporcionen el poder predictivo.

[1] Fuente:<a href="https://docs.microsoft.com/es-es/azure/machine-learning/studio/algorithm-choice" class="uri">https://docs.microsoft.com/es-es/azure/machine-learning/studio/algorithm-choice</a>

[2] Fuente:
<a href="http://www.kdnuggets.com/2016/11/machine-learning-vs-statistics.html" class="uri">http://www.kdnuggets.com/2016/11/machine-learning-vs-statistics.html</a>

[3] Ver
<a href="https://www.quora.com/What-is-the-difference-between-statistics-and-machine-learning" class="uri">https://www.quora.com/What-is-the-difference-between-statistics-and-machine-learning</a>
