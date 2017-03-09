# ANNs
## Artificial Neural Networks (Implementacion con Java)

En la d�cada de 1940, el neurofisi�logo Warren McCulloch y el matem�tico
Walter Pits dise�� la primera implementaci�n matem�tica de una neurona artificial
Combinando los fundamentos de la neurociencia con las operaciones matem�ticas. A eso
Tiempo, se estaban llevando a cabo muchos estudios sobre la comprensi�n del cerebro
C�mo y si se podr�a simular, pero dentro del campo de la neurociencia. La idea
De McCulloch y Pits fue una verdadera novedad porque agreg� el componente de matem�ticas.
Adem�s, considerando que el cerebro est� compuesto de miles de millones de neuronas, cada una
Interconectado con otro mill�n, lo que resulta en unos billones de conexiones,
Est�n hablando de una estructura de red gigante. Sin embargo, cada unidad neuronal es muy
Simple, actuando como un mero procesador capaz de sumar y propagar se�ales.

Bas�ndose en este hecho, McCulloch y Pits dise�aron un modelo sencillo para
Neurona �nica, inicialmente para simular la visi�n humana. Las calculadoras disponibles o
Las computadoras en ese momento eran muy raras pero capaces de tratar con
Operaciones bastante bien; Por otro lado, incluso hoy en d�a tareas como la visi�n y el sonido
Reconocimiento no son f�cilmente programables sin el uso de frameworks especiales,
Opuesto a las operaciones y funciones matem�ticas. Sin embargo, el
Cerebro puede realizar estas �ltimas tareas m�s eficientemente que las primeras, y este hecho
Realmente instiga a cient�ficos e investigadores.

Por lo tanto, una ANN se supone que es una estructura para realizar tareas como el patr�n
Reconocimiento, aprendiendo de los datos, y las tendencias de pron�stico, al igual que un experto puede hacer en
La base del conocimiento, en oposici�n al enfoque algor�tmico convencional que
Requiere un conjunto de pasos a realizar para lograr un objetivo definido. An ANN en su lugar
Tiene la capacidad de aprender a resolver alguna tarea por s� misma, debido a su alta
Estructura de red interconectada.

### El elemento mas b�sico : "Neurona Artificial"

Las neuronas naturales han demostrado ser procesadores de se�ales ya que reciben micro se�ales
En las dendritas que pueden desencadenar una se�al en el ax�n dependiendo de su fuerza o
magnitud. Podemos entonces pensar en una neurona como tener un colector de se�al en las entradas
Y una unidad de activaci�n en la salida que puede activar una se�al que ser� reenviada
A otras neuronas. Por lo tanto, podemos definir la estructura de la neurona artificial como se muestra en la
Siguiente figura:


### Dar vida a las neuronas: Funcion de Activacion


La salida de la neurona viene dada por una funci�n de activaci�n. Este componente a�ade
No linealidad al procesamiento de la red neuronal, que es necesario porque el
La neurona tiene conductas no lineales. Una funci�n de activaci�n suele estar limitada entre
Dos valores en la salida, siendo por lo tanto una funci�n no lineal, pero en algunos
Casos, puede ser una funci�n lineal.
Las cuatro funciones de activaci�n m�s utilizadas son las siguientes:

* Sigmoide
* Tangente hiperb�lica
* Umbral de limitaci�n dif�cil
* Puramente lineal


![](https://i.imgur.com/Bwu1Qib.png)

### Los valores fundamentales - pesos

En las redes neuronales, los pesos representan las conexiones entre las neuronas y tienen la capacidad de amplificar o atenuar las se�ales neuronales, por ejemplo, multiplicar las se�ales, Modific�ndolos as�. Por lo tanto, mediante la modificaci�n de las se�ales de red neuronal, los pesos neuronales Tienen el poder de influir en la salida de una neurona, por lo tanto la activaci�n de una neurona Depender de las entradas y de los pesos. Siempre que los insumos provienen tras neuronas o del mundo externo, los pesos se consideran un neural Conexiones establecidas de la red entre sus neuronas. Por lo tanto, puesto que los pesos son
Interno de la red neuronal e influir en sus resultados, podemos considerarlos como Conocimiento de redes neuronales, siempre que cambiar los pesos cambie la Las capacidades de la red neural y por lo tanto las acciones.

## Las partes que forman las capas enteras

Las neuronas naturales se organizan en capas, cada una proporcionando un nivel espec�fico de
tratamiento; Por ejemplo, la capa de entrada recibe est�mulos directos desde el exterior
Mundo, y las capas de salida activan acciones que tendr�n una influencia directa en la
mundo exterior. Entre estas capas, hay una serie de capas ocultas, en el
Sentido de que no interact�an directamente con el mundo exterior. En el neural artificial
Todas las neuronas de una capa comparten las mismas entradas y la misma funci�n de
Que se muestra en la siguiente figura:

![](https://i.imgur.com/5edtDMk.png)

Las redes neuronales pueden estar compuestas de varias capas vinculadas, formando los llamados
Redes multicapa. Las capas neurales se pueden dividir b�sicamente en tres clases:

* Capa de entrada
* Capa oculta
* Capa de salida

En la pr�ctica, una capa neural adicional a�ade otro nivel de abstracci�n de la Fuera de los est�mulos, aumentando as� la capacidad de la red neural para representar m�s complejos conocimiento .


## Sobre Arquitecturas la red neuronal

B�sicamente, una red neuronal puede tener diferentes dise�os, dependiendo de c�mo Neuronas o capas neuronales est�n conectadas entre s�. Cada red neuronal La arquitectura est� dise�ada para un fin espec�fico. Las redes neuronales se pueden aplicar a
N�mero de problemas y, dependiendo de la naturaleza del problema, los Red debe ser dise�ada con el fin de abordar este problema de manera m�s eficiente.

B�sicamente, hay dos modalidades de arquitecturas para redes neuronales:

* Conexiones neuronales
	+ Redes monocapa
	+ Redes multicapa
* Flujo de se�al
	+ Redes de feedforward
	+ Redes de retroalimentaci�n
	
### Redes monocapa

En esta arquitectura, todas las neuronas se presentan en el mismo nivel, formando una sola, Como se muestra en la siguiente figura:

![](https://i.imgur.com/awSjDyr.png)

La red neuronal recibe las se�ales de entrada y las alimenta en las neuronas, que A su vez producen las se�ales de salida. Las neuronas pueden estar altamente conectadas a Otras con o sin recurrencia. Ejemplos de estas arquitecturas son la capa �nica
Perceptron, Adaline, mapa auto-organizativo, redes neurales de Elman y Hopfield.

## Redes multicapa

En esta categor�a, las neuronas se dividen en m�ltiples capas, cada capa correspondiente A una distribuci�n paralela de neuronas que comparte los mismos datos de entrada, como se muestra en el Siguiente figura:

![](https://i.imgur.com/Om9Ply7.png)

Las funciones de base radial y perceptrones multicapa son buenos ejemplos de esto
arquitectura. Estas redes son realmente �tiles para aproximar datos reales a
Funci�n especialmente dise�ada para representar esos datos. Adem�s, debido a que
M�ltiples capas de procesamiento, estas redes est�n adaptadas para aprender de las
Datos, pudiendo separarlo o determinar m�s f�cilmente el conocimiento que
Reproduce o reconoce estos datos.


## Redes de feedforward

El flujo de las se�ales en redes neuronales puede estar en una sola direcci�n o en
reaparici�n. En el primer caso, llamamos a la arquitectura de red neuronal feedforward,
Puesto que las se�ales de entrada son alimentadas a la capa de entrada; Despu�s, despu�s de ser procesado,
Son reenviados a la capa siguiente, tal como se muestra en la figura en la capa m�ltiple
secci�n. Los perceptrones multicapa y las funciones de base radial son tambi�n buenos ejemplos de
Redes de feedforward.


### Feedback networks

Cuando la red neuronal tiene alg�n tipo de recurrencia interna, significa que Las se�ales se retroalimentan en una neurona o capa que ya ha recibido y Procesado esa se�al, la red es del tipo de retroalimentaci�n. Vea el siguiente
Figura de redes de retroalimentaci�n:

![](https://i.imgur.com/Dt0Lced.png)

La raz�n especial para a�adir recurrencia en la red es la producci�n de una din�mica
Comportamiento, particularmente cuando la red soluciona problemas relacionados con
O reconocimiento de patrones, que requieren una memoria interna para reforzar el aprendizaje
proceso. Sin embargo, estas redes son particularmente dif�ciles de entrenar,
aprender. La mayor�a de las redes de retroalimentaci�n son de capa �nica, como Elman y Hopfield
Redes, pero es posible construir una red multicapa recurrente, como eco y
Recurrentes multicapas.

## De la ignorancia al proceso de aprendizaje del conocimiento

Las redes neuronales aprenden ajustando las conexiones entre las neuronas, a saber:
los pesos. Como se menciona en la secci�n de estructura neural, los pesos representan la
Conocimiento de redes neuronales. Diferentes pesos hacen que la red produzca
Resultados para las mismas entradas. As�, una red neuronal puede mejorar sus resultados adaptando
Sus pesos seg�n una regla de aprendizaje. El esquema general del aprendizaje se representa en
La siguiente figura:

![](https://i.imgur.com/0WlQIgZ.png)

La figura anterior se llama aprendizaje supervisado porque Hay una salida deseada, pero las redes neurales pueden aprender s�lo por los datos de entrada, Sin ninguna salida deseada (supervisi�n). Luego veremos C�mo aprenden las redes neuronales,
Vamos a profundizar en el proceso de aprendizaje de la red neuronal.


