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
\text{Tipo de Galleta} & \text{Tipo de Galleta} & \text{Ganancia} & \text{Harina Req} & \text{Levadura Req} \\
 \hline \hline
 \text{Vainilla}           & $1200 & $600 & 20 g & 2 g \\
 \text{Chips de Chocolate} & $1500 & $750 & 18 g & 3 g \\
 \hline
 \text{Total Disponible}   &       & & 2000 g & 250 g \\
 \hline
\end{array}
$$
