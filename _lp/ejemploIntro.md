---
layout: post
title: Formulando un problema
use_math: true
---

Vamos a comenzar con un ejemplo sencillo, en las próximas secciones abordaremos las preguntas planteadas anteriormente y desarrollaremos los consptos básicos de la programación lineal.

_Suponga que usted desea mejorar su situación económica en la universidad y planea vender galletas caseras a sus compañeros de clase. La receta familiar que usted posee garantiza la venta de todas las galletas que fabrique, pero los ingredientes con los que cuenta usted y la capacidad de su horno limita considerablemente su producción, así que debe organizarla de la mejor manera_. 

_Usted puede fabricar galletas de vainilla y galletas de chips de chocolate. Las primeras las vende a un precio de $1200 la unidad y las segundas a $1500 cada una. La receta usa como ingredientes principales harina refinada (importada) y levadura francesa, los otros ingredientes se consiguen fácilmente y por lo tanto no le preocupan. Cada semana, su hermana le envía por encomienda 2000 g de harina y 250 g de levadura. Cada galleta de vainilla requiere de 20 g de harina y 2 g de levadura, mientras que una de chips de chocolate usa 18 g de harina y 3 g de levadura. Adicionalmente, en su horno puede hornear un máximo de 20 galletas diarias, de cualquier clasde, de lunes a viernes que son los días que usted va a la universidad_. 

_Si el margen de ganacia de cada galleta es del 50%, ¿cuál debería ser su plan de producción semanal para maximizar su ganacia?_

#### Solución

Vamos a desarrollar el modelo con todos sus elementos, cada uno de ellos respondiendo a una pregunta relevante para el problema

##### Variables de Decisión

La pregunta clave aquí es **¿Qué debe decidirse?**, en este caso la respuesta corresponde al número de galletas de cada tipo que usted debe fabricar cada semana, formalmente se definen dos variables de la siguiente forma:

$$
\begin{align*}
   X_1&: \text{ Cantidad de galletas de vainilla a fabricar cada semana}\\
   X_2&: \text{ Cantidad de galletas de chips de chocolate a fabricar cada semana}
\end{align*}
$$

##### Parámetros

 La pregunta clave en este caso es **¿Qué información se encuentra disponible para tomar la decisión?**, en este problema tenemos para cada galleta, el precio de venta, de donde obtenemos la ganacia unitaria; el requerimiento de cada tipo de materia prima para cada galleta; la cantidad semanal disponible de cada tipo de materia prima y la capacidad diaria del horno, la que se puede llevar a una capacidad semanal. En resumen los parámetros del problema son:
 
 
$$
\begin{array} {l|cccc}
\text{Tipo de Galleta} & \text{Precio} & \text{Ganancia} & \text{Harina} & \text{Levadura} \\
 \hline \hline
 \text{Vainilla}           & $1200 & $600 & 20 g & 2 g \\
 \text{Chips de Chocolate} & $1500 & $750 & 18 g & 3 g \\
 \hline
 \text{Total Disponible}   &       & & 2000 g & 250 g \\
 \hline
\end{array}
$$

##### Restricciones

Ahora es el turno de responder la pregunta **¿Qué limita la decisión?**, es decir, qué impide que se fabriquen miles y miles de galletas semanalmente. En este caso, las limitaciones vienen dadas por las dos materias primas y por la capacidad del horno. 

Primero consideremos la disponibilidad de harina, si sólo se fabricaran galletas de vainilla, se consumen 20 g por cada galleta fabricada, como se van a fabricar $$ X_1 $$ 
galletas de vainilla, el gasto de harina sería de $$ 20X_1 $$
, por otra parte, al considerar las galletas de chips de chocolate, se tiene que su consumo de harina sería de $$ 18X_2$$
, así el consumo total de harina sería la suma de las dos cantidades halladas, es decir, $$ 20X_1 + 18X_2$$
. Dicho consumo no debe sobrepasar la cantidad semanal de harina disponible, esto en forma de una desigualdad se expresa como:
$$
\begin{align}
20X_1 + 18X_2 \leq 2000
\end{align}
$$

De una forma equivalente, al considerar la levadura se tiene que el consumo para las galletas de vainilla es de $$ 2X_1$$
, mientras que el consumo de levadura de las galletas de chips de chocolate es de $$ 3X_2$$
. Por lo tanto, el consumo total de levadura sería la suma de las dos cantidades, es decir, $$ 2X_1 + 3X_2$$
, la cual no debe superar la disponibilidad semanal de levadura, así tenemos la siguiente desigualdad:
$$
\begin{align}
2X_1 + 3X_2 \leq 250
\end{align}
$$

Finalmente, se dispone de 5 días para hornear las galletas y cada día se pueden hornear 20 de ellas, es decir, en la semana se pueden hornear en total 100 galletas, así la suma total de las galletas fabricadas, las de vainilla más las de chips de chocolate, no debe ser mayor que 100, en forma de desigualdad esto sería:
$$
\begin{align}
X_1 + X_2 \leq 100
\end{align}
$$
