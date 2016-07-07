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



