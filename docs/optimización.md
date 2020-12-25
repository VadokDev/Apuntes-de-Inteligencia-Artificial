---
id: optimización
title: Optimización
---

### Optimización

Determinación de una alternativa de decisión con la propiedad de ser mejor que cualquier otra en algún sentido a precisar

- **Función objetivo**: Medida cuantitvativa del funcionamiento del sistema que se desea optimizar
- **Variables**: Decisiones que se puedne tomar para afectar el valor de la función objetivo
- **Restricciones**: Relaciones (ecuaciones e inecuaciones) que las variables están obligadas a cumplir
- **Parámetros**: Atributos del problema conocidos a priori y fijos que permiten simplificar la formulación del modelo

Resolver un problema de optimización significa encontrar el valor de las variables que optimiza la función objetivo y satisface todas las restricciones, o bien, detectar que el problema planteado no tiene solución.

### Importancia del Modelado

Modelar problemas permite eliminar toda ambigüedad a la hora de expresar el problema, de modo tal que éste se entienda y el modelo sirva como mecanismo de comunicación del mismo, a su vez, modelar un problema permite identificar semenjanzas de éste con problemas clásicos, lo que puede guiar a encontrar mecanismos de resolución que se puedan aplicar a nuestro problema modelado.

### Clasificación de Modelos de Optimización

- Programación lineal (continua)
- Programación lineal entera mixta
- Programación no lineal

### Problema de la Dieta

Las necesidades mínimas en la alimentación de una ternera son de 700 [g] de proteínas, 28 [g] de calcio y 150 [mg] de vitaminas. Los alimentos disponibles son pienso (alimento seco que se le da al ganado) y forraje con un costo de 0.30 y 0.34 euros/kg respectivamente. La composición nutritiva por kg:

|           | Proteínas [g] | Calcio [g] | Vitaminas [mg] |
| :-------: | :-----------: | :--------: | :------------: |
| Pienso 	| 		30		| 	   2	 | 		 10		  |
| Forraje	| 		45		|	   1	 | 		 5		  |

Se trata de determinar la cantidad diaria óptima de cada alimento para minimizar el costo total de alimentación


**Fundamental Theorem of Calculus**  
Let $f:[a,b] \to \R$ be Riemann integrable. Let $F:[a,b]\to\R$ be $F(x)=
\int_{a}^{x}f(t)dt$.
Then $$F$$ is continuous, and at all $x$ such that $f$ is continuous at $x$,
$F$ is differentiable at $x$ with $F'(x)=f(x)$.

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
* Se debe cumplir con la necesidad mínima de cada nutriente indicado en $NM_{j}$, notar que las unidades de los nutrientes están expresadas en gramos y miligramos, no obstante, las variables involucradas en la restricción son consistentes pues $X_{i}$ está en kilos y $CN_{ij}$ está $\frac{g}{kilos}$ por lo que el lado izquierdo de la expresión queda en $g$, por otra parte el lado derecho de la expresión sólo involucra a $NM_{j}$ el cual está expresado en $g$, por lo que la ecuación es consistente.

$$
\sum_{i} 
	X_{i} \cdot CN_{ij} \geq NM_{j} \forall j
$$
