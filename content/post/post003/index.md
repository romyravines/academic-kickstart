---
title: 'Mis ventas: ¿Series temporales?'
subtitle: '¿Como trabajar con datos históricos?'
summary: Las ventas tienen características particulares que deben tenerse en cuenta al hacer modelos y obtener previsiones.
authors:
- admin
tags: ["Forecasting"]
categories: ["Statistics"]
date: "2016-04-20T00:00:00Z"
lastmod: "2019-04-17T00:00:00Z"
featured: false
draft: false
math: true

# Featured image
image:
  caption: ''
  focal_point: ""
  preview_only: false

# Projects (optional).
projects: []

---

{{% alert note %}}
Una serie temporal (o simplemente una serie) es una secuencia de N observaciones ordenadas y equidistantes cronológicamente sobre una característica o varias características de una unidad observable en diferentes momentos. 
{{% /alert %}} 

 * Si la serie es sobre una característica se dice que es univariante o escalar. 
 * Si la serie es sobre dos o más características se dice que es multivariante o vectorial.


El estudio de las series temporales permite: (1) entender mejor el mecanismo de generación de los datos, que puede no ser claro inicialmente en una investigación y/o (2) hacer pronósticos sobre el futuro, es decir: previsiones. Las previsiones se utilizan en forma constante en diversos campos: economía, finanzas, marketing, medio ambiente, ingeniería, etc. En general, las previsiones proporcionan una guía para las decisiones que deben tomarse.

Algunos ejemplos de uso de las previsiones son:

 * En **Planeamiento y Control de Operaciones**. Las decisiones de producción de un artículo con base en los pronósticos de ventas. Es posible por ejemplo, detectar una disminución en la tendencia de ventas que conlleve a reducir la producción, o al contrario.
 
 * En Marketing. La decisión de invertir en publicidad puede depender de prever las ventas.
 
 * En **Economía**. Las decisiones del Banco de España, por ejemplo para el control de la inflación, requieren la previsión y el examen del comportamiento de ciertas variables macroeconómicas, como el PIB, la tasa de desempleo, el IPC, las tasas de interés a distintos plazos, activas y pasivas.
 
 * En **Turismo**. La previsión del de número de turistas mensuales para determinar la demanda hotelera.
 
 * En **Epidemiología** y **Medio Ambiente**. La vigilancia de los niveles de contaminantes en el aire tiene como herramienta fundamental las series de tiempo. Pero adicionalmente el efecto de estos niveles sobre la salud

Todas las series temporales tienen características particulares. Asi por ejemplo, las series pueden:

 * evolucionar alrededor de un nivel constante o tienen tendencias crecientes o decrecientes, 
 * evolucionar alrededor de un nivel que cambia sin seguir aparentemente un patrón concreto - tienen tendencia estocástica - 
 * presentar reducciones (en invierno) y aumentos (en verano) sistemáticos en su nivel cada 12 meses - son estacionales -
 * presentar variabilidad constante alrededor de su nivel
 * presentar variabilidad condicional o alta volatilidad,
 * moverse conjuntamente con otras series - tendencia común -
 * etc.


En las secciones siguiente se describen brevemente algunos conceptos necesarios para la modelación básica de series temporales.

## Operadores 

### Operador de retardo simple

El operador de retardo simple se define como

$$
Bz_t=z_{t-1}
$$

Si aplicamos el operador de retardo dos veces:

$$BBz_t=Bz_{t-1}=z_{t-2}$$

Del mismo modo, si aplicamos $n$ veces el operador de retardo, obtenemos:

$$ BB \ldots Bz_t=z_{t-n} $$

Definimos, por tanto

$$ B^n z_t=z_{t-n} $$

### Operador de adelanto simple
De modo análogo, definimos el **operador de adelanto simple**

$$
    Fz_t&=z_{t+1}\\
    F^n z_t&=z_{t+n}
$$

El operador $F$ es el inverso del operador $B$ ya que:

$$
FBz_t=BFz_t=z_t
$$
Por tanto, $BF=FB=1,$ lo que implica que $F=B^{-1}$.

### Polinomios en B

Sea el polinomio en el operador de retardo $B$:
$$
\phi_0 - \phi_1 B - \ldots - \phi_pB^p
$$
La operación de este polinomio se define como:
$$
(\phi_0 - \phi_1 B - \ldots - \phi_pB^p)z_t=\phi_0z_t+\phi_1z_{t-1}+\ldots+\phi_pz_{t-p}
$$
Llamamos **polinomio autorregresivo** de orden $p$ al polinomio de grado $p$
$$
1-\phi_1B-\dots-\phi_pB^p
$$
La razón de esta nomenclatura es que si tenemos una serie cuyo comportamiento puede expresarse como
$$
(1-\phi_1B-\dots-\phi_pB^p)z_t=e_t
$$
donde $e_t$ es un término de error, la anterior expresión puede escribirse como:
$$
    z_t=\phi_1 z_{t-1}+ \ldots + \phi_p z_{t-p} + e_t
$$

Es decir, como una regresión donde la serie $z_t$ es el output y los propios retardos $1,2,\ldots,p$ de la variable actúan como *inputs* o regresores construyendo una **autorregresión**.

En muchas ocasiones emplearemos las formas $\phi(B), \psi(B), \varphi(B)$ u otras semejantes para denotar polinomios en $B$. Notaremos más adelante que asociaremos ciertas formas de expresar polinomios en $B$ como $\phi(B)$ a clases de polinomios en $B$ que juegan cierto papel especial. Por ejemplo, reservaremos la expresión $\phi(B)$ a polinomios autorregresivos.

### Operador diferencia

El operador diferencia respecto al pasado, en lo sucesivo simplemente **operador diferencia**, se define como:
$$
\bigtriangledown z_t = z_t - z_{t-1},
$$
que puede expresarse como:
$$
\bigtriangledown z_t = z_t - z_{t-1},
$$
que puede expresarse como
$$
(1-B)z_t=\bigtriangledown z_t.
$$
Por lo tanto: $\bigtriangledown =1-B$.
El operador de \textbf{diferencia periódica}, usualmente **diferencia estacional**, se define como
$$
\bigtriangledown_s z_t=z_t-z_{t-s}=(1-B^s)z_t.
$$
Luego, $\bigtriangledown_s=(1-B^s).$

Debe observarse que cuando aplicamos el operador $B$ a una serie $S$ lo que hacemos en realidad es **adelantar** la serie un periodo. Homólogamente, cuando aplicamos el operador $F$ a una serie $S$ **retrasamos** la serie un periodo.

## Alisado Exponencial

### ¿Qué es el Alisado Exponencial?


 * Es una técnica aplicada a series de tiempo, para ``suavizarlas'' u obtener previsiones.
 * Mientras que, con la media móvil, las observaciones pasadas se ponderan por igual, en el alisado exponencial se asignan ponderaciones exponencialmente decrecientes en el tiempo.
 * La fórmula utilizada es:
 
   $$ y_1 = x_0  $$
   $$ y_t = (1-\theta)x_{t-1}+\theta y_{t-1},  t > 1 $$



donde $\{x_t\}$ son las observaciones reales, $\{y_t\}$ son las estimaciones y  $\theta$ es el factor de alisamiento, $0 < \theta < 1$.
        
 En otras palabras, con este método, la previsión para el periodo $t$ (valor esperado) como la suma ponderada de todas la observaciones anteriores, dando mayor importancia a las observaciones más recientes que a las más antiguas. Como puede verse en:
 
$$ y_t = (1-\theta) x_{t-1} +\theta y_{t-1} $$ 
$$ y_t = (1-\theta)x_{t-1}+(1-\theta)\theta x_{t-2}+(1-\theta) \theta^2 y_{t-2} $$

$$ y_t = (1-\theta)[x_{t-1}+\theta x_{t-2}+\theta x_{t-3}+\theta x_{t-4}+ ...] + \theta^{t-1} x_0 $$ 

            
  Así, los pesos asignados a las observaciones previas pertenecen a una proporción de la progresión geométrica: $\{1, \theta, \theta^2, \theta^3, ..\}$.
            
 * Por otro lado, si la ecuación arriba se expresa como: 

$$
                y_t = x_{t-1} + \theta(y_{t-1} - x_{t-1}) ,  
$$
            
Se aprecia que $y_t$ está formada por la suma de la observación en el periodo anterior ($x_{t-1}$) más una proporción ($\theta$) del error cometido ($y_{t-1} - x_{t-1}$). Por lo tanto el valor de $\theta$ controla la rapidez con que la previsión se adapta a los cambios del nivel de la serie (estado).
            
 * Si $\theta$ es grande (próximo a 1), la previsión se adapta rápidamente a los cambios, por lo tanto se debe utilizar en series poco estables.
 * Si $\theta$ es pequeño (próximo a 0), se consigue eliminar el efecto de las fluctuaciones, por lo tanto se debe utilizar en series estables.
 * El valor de $\theta$ se puede optimizar minimizando la suma de cuadrados del error de previsión, es decir, resolviendo: $min(x_{t-1} - y_{t-1})^2$.
 * El alisado exponencial, técnicamente, es equivalente a un modelo *ARIMA (0,1,1)* sin constante. En otras palabras, se puede representar por:
$$             \hat{y} = (1-\theta)(1 + \theta B + \theta^2 B^2 + \theta^3 B^3 + ...)x_{t-1}
$$
 donde B es el operador retardo y $\theta$ es el parámetro de amortiguamiento. Esta representación no implica recargar el último término con un peso mayor a los valores más recientes.
            Si existe un número finito de períodos observados, la ecuación anterior se reescribe como:
            
$$ \hat{y} = \alpha (1 + \theta B + \theta^2 B^2 + ... + \theta^p B^p)x_{t-1}$$
            
 donde $p$ es el número de periodos disponibles y $\alpha <1 $ es un término que asegura que los coeficientes de la ecuación sumen la unidad. Eso permite que el peso relativo de cada uno de los datos del pasado se mantenga constante y, al mismo tiempo, el resultado siga siendo una media.
            
 * En la tabla abajo  se muestran los pesos que toman los términos en el caso de contar con 6 términos.

 |                   | I    | II      | III       | IV      | V   |
 | :-------------             |:----------:| ----------:| ----------:| ----------:| ----------:|
 | $\theta$                   | 0.70      | 0.65       | 0.60       | 0.55        | 0.50    |
 | $(1- \theta)$              | 0.30      | 0.35      | 0.40       | 0.45        | 0.50    |
 | $(1- \theta)\theta$       | 0.21      | 0.23      |    0.24      |    0.25   |    0.25    |
 | $(1- \theta)\theta^2$     | 0.15      | 0.15      |    0.14      |    0.14   |    0.13    |
 | $(1- \theta)\theta^3$     | 0.10      | 0.10      |    0.09      |    0.07   |    0.06    |
 | $(1- \theta)\theta^4$     | 0.07      | 0.06      |    0.05      |    0.04   |    0.03    |
 | $(1- \theta)\theta^5$     | 0.05      | 0.04      |    0.03      |    0.02   |    0.02    |
 

  
