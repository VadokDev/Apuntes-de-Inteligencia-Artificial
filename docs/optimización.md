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

### Instancia

Una instancia se define como caso particular de un problema general, en general un mismo modelo puede resolver distintas instancias que derivan de un mismo problema, por eso a lo largo del curso se verán modelos generales de problemas generales.

### Modelado con Variables Enteras y Binarias

El uso de variables enteras y binarias aumenta considerablemente las posibilidades de modelado, permitiendo:
* Modelado de cantidades discretas
	* Hablar de 3 personas y no 3.5 pues esto deja de tener sentido
* Modelado de decisiones que implican un costo fijo o de arranque: 
	* Adquirir o no un activo (un edificio, una máquina, etc.)
	* Poner en marcha un proceso o no
* Modelado de decisiones que posibilitan la toma de otras decisiones:
	* La compra de un determinado aparato (variable binaria) permite después tomar decisiones relativas a su operación
	* Contratar más personal, personal especializado, personal no especializado, etc.
* Modelado de restricciones no lineales y no convexas
* Modelado de implicaciones y condiciones lógicas
	* El resultado de cierta variable condiciona el hecho de que otra restricción tiene que cumplirse o no

### Espacio de Búsqueda

A la hora de resolver un problema, se generarán distintas alternativas que serán candidatas a ser soluciones del problema, no obstante, algunas de éstas pueden no satisfacer las restricciones que el problema impone y por tanto considerarse **infactibles**. El conjunto de todas las posibilidades de soluciones para el problema, es decir, tanto las factibles como las infactibles, será el espacio de búsqueda del problema, cuyo tamaño generalmente se puede calcular (especialmente en problemas de combinatoria, donde su tamaño será la cantidad total de combinaciones distintas que éste tenga).

El tamaño del espacio de búsqueda generalmente crece cuando el tamaño del problema lo hace, y cuando éste crecimiento es de manera exponencial o factorial, se dice que hay una **explosión combinatoria**. No obstante, si las variables del problema son reales, dado que entre un número y otro hay infinitos números, el espacio de búsqueda pasa a ser infinito y por ende, no se puede calcular su tamaño. 

### Resolución por Fuerza Bruta

Procedimiento capaz de probar todas las combinaciones posibles del espacio de búsqueda y evaluar la factibilidad de cada una, eligiendo la que mejor optimice la función objetivo o bien, determinando que el problema no tiene solución