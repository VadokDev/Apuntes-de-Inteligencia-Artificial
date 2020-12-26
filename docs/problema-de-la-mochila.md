---
id: problema-de-la-mochila
title: Problema de la Mochila
---

El problema de la mochila, mejor conocico como Knapsack Problem, modela una situación análoga al llenado de una mochila que soporta un peso determinado, con todo o parte de un conjunto de objetos donde cada uno tiene un peso y valor específico. Los objetos colocados en la mochila deben maximizar el valor total sin exceder el peso máximo de la misma.

| Mochila: 15kg	|			| Objeto 1	| Objeto 2	|	Objeto 3	|
|	---:		|	:---:	|	:---:	|	:---:	|	 :-----:	|
| Peso			|			|	 5kg	|	15kg	|		10kg	|
| Valor			|			|	 $15	|	$1		|		$10		|

### Modelo Matemático

** Variables: ** 

* Usaremos una variable de decisión, asociada a llevar o no un objeto

$$
X_{i} = \left\{ \begin{array}{cc} 
                1 & \hspace{5mm} \text{si llevo el objeto } i \\
                0 & \hspace{5mm} \text{si no lo llevo} \\
                \end{array} \right.
$$

** Parámetros: **

* $C:$ Capacidad de la mochila
* $n:$ Cantidad de objetos
* $V_{i}:$ Valor del objeto $i$
* $P_{i}:$ Peso del objeto $i$

** Función Objetivo: **
* La función debe maximizar el costo total de los objetos insertados en la mochila
$$
\text{Max}
\sum_{i} 
	V_{i} \cdot X_{i}
$$

** Restricciones: **
* La mochila no puede soportar más peso del determinado en $C$ (según la instancia que se esté resolviendo), por lo tanto, se debe procurar que el costo de todos los objetos insertados en ella sea menor o igual al peso máximo de la mochila

$$
\sum_{i} 
	P_{i} \cdot X_{i} \leq C
$$

Éste se conoce como un problema de optimización combinatoria pura pues utiliza únicamente variables binarias.