---
id: problema-de-la-dieta
title: Problema de la Dieta
---

Las necesidades mínimas en la alimentación de una ternera son de 700 [g] de proteínas, 28 [g] de calcio y 150 [mg] de vitaminas. Los alimentos disponibles son pienso (alimento seco que se le da al ganado) y forraje con un costo de 0.30 y 0.34 euros/kg respectivamente. La composición nutritiva por kg:

|           | Proteínas [g] | Calcio [g] | Vitaminas [mg] |
| :-------: | :-----------: | :--------: | :------------: |
| Pienso 	| 		30		| 	   2	 | 		 10		  |
| Forraje	| 		45		|	   1	 | 		 5		  |

Se trata de determinar la cantidad diaria óptima de cada alimento para minimizar el costo total de alimentación

### Modelo Matemático

** Variables:** 

* $X_{i}:$ Kilos a comprar del alimento $i$

** Parámetros: **
* $C_{i}:$ Costo / Kilo del alimento $i$, con $i \in \{\text{pienso, forraje}\}$
* $NM_{j}:$ Necesidad mínima del nutriente $j$, con $j \in \{\text{proteínas, calcio, vitaminas}\}$
* $CN_{ij}:$ Composición nutricional del alimento $i$ respecto del nutriente $j$

** Función Objetivo: **
* Dado que se requiere minimizar los costos, la F.O. se expresa como el costo total de comprar $x$ kilos del alimento $i$

$$
\text{Min}
\sum_{i} 
	C_{i} \cdot X_{i}
$$

** Restricciones: **
* Se debe cumplir con la necesidad mínima de cada nutriente indicado en $NM_{j}$, notar que las unidades de los nutrientes están expresadas en gramos y miligramos, no obstante, las variables involucradas en la restricción son consistentes pues $X_{i}$ está en kilos y $CN_{ij}$ está en $\left[\frac{g}{kilos}\right]$ por lo que el lado izquierdo de la expresión queda en $g$, por otra parte el lado derecho de la expresión sólo involucra a $NM_{j}$ el cual está expresado en $g$, por lo que la ecuación es consistente.

$$
\sum_{i} 
	X_{i} \cdot CN_{ij} \geq NM_{j} \text{ } \forall j
$$

* Otras restricciones son las de no-negatividad, vale decir: $X_{i} \geq 0 \text{ } \forall i$

Éste modelo es lo suficientemente general como para asociarse a cualquier problema derivado de **El Problema de la Dieta**, además, dado que todas sus variables admiten valores reales, el problema queda categorizado como un **Problema de Programación Lineal**
