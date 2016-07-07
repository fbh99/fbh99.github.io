---
layout: post
title: Formulación de Programas Lineales
use_math: true
---

En esta sección veremos los principios básicos que se deben seguir para formular un problema como un programa lineal. Sin embargo, es importante notar que no existe una receta única para formular problemas y que cada caso debe ser abordado con cuidado.

En general, si podemos caracterizar el tipo de problemas que abordaremos en este curso por sus componentes principales:

  - Es un problema de optimización 
  - Se tiene una única fución objetivo
  - Las variables de decisión son variables continuas no negativas
  - El problema está restringido
  - Tanto la función objetivo, como cada una de las restricciones son funciones lineales en las variables del problema

En algunos casos la tercera condición estará acompañada por una más estricta para un subconjunto de las variables de decisión, exigiendo que las variables sean enteras no negativas o, restringuiendo aún más, que las variables sean binarias (variables que sólo toman valores de 0 o 1). En cualquiera de los casos el problema ya no es un programa lineal, se le conoce como programa entero mixto.

Antes de comenzar con los modelos prototipo se deben hacer unas pequeñas aclaraciones:

Al tratarse de un problema de optimización, se buscan los valores extremos globales que toma la función objetivo, estos pueden ser un máximo o un mínimo, cuál de los dos se obtiene dependerá del criterio de optimización utilizado: **maximizar** o **minimizar**.

Aunque hay variantes en donde se tienen múltiples funciones objetivo que se buscan optimizar, en este curso nos centramos en los problemas con una única función objetivo. Ésta debe ser lineal, es decir, una combinación lineal de la variables de decisión:

$$
\begin{align}
c_1X_1 + c_2X_2 + \cdots + c_nX_n
\end{align}
$$

Los valores $$c_1, c_2, \ldots, c_n$$ son los coeficientes de la combinación y se asumiran conocidos de antemano, determinísticos e independientes de las variables de decisión. Algunos de esos valores pueden ser 0 si la variable asociada no contribuye a la función objetivo. 

Note que la forma funcional de la función objetivo es única, para ser lineal siempre debe tener esta forma, eso excluye funciones con términos tales como: $$X_i^2$$ o $$\sqrt{X_i}$$ o $$X_i^n$$ donde el $$n$$ esduferente de 1, tampoco se tienen términos de la forma $$X_i\cdot X_j$$ o $$\ln{X_i}$$ o cualquier otra función no lineal. 

En algunos casos se tendrán variables que tienen un dominio continuo, en ese caso el programa no será lineal pero como existen algoritmos de solución eficientes para muchos de esos casos, se usarán variables enteras (incluyendo las binarias) en los modelos de este curso. Adicionalmente, si se tiene una variable no restricta, es decir, que puede tomar valores negativos así como mayores o iguales que 0, siempre se podrá llevar a una combinación de variables no negativas, así que este caso no será un problema para los modelos. 