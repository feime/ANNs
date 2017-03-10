# ANNs
## Artificial Neural Networks (Implementacion con Java)

En la década de 1940, el neurofisiólogo [Warren McCulloch](https://es.wikipedia.org/wiki/Warren_McCulloch) y el matemático
[Walter Pits](https://es.wikipedia.org/wiki/Walter_Pitts) diseñó la primera implementación matemática de una neurona artificial
Combinando los fundamentos de la neurociencia con las operaciones matemáticas. En ese
Tiempo, se estaban llevando a cabo muchos estudios sobre la comprensión de Cómo se podria simular el cerebro

La idea De McCulloch y Pits fue una verdadera novedad porque agregó el componente de las matemáticas.
Además, considerando que el cerebro está compuesto de miles de millones de neuronas, cada una
Interconectado con otro millón, lo que da de resultado unos billones de conexiones,
Estamos hablando de una estructura de red gigante. Sin embargo, cada unidad neuronal es muy
Simple, actuando como un mero procesador capaz de sumar y propagar señales.

Basándose en este hecho, McCulloch y Pits diseñaron un modelo sencillo para
Neurona única, inicialmente para simular la visión humana. Las calculadoras disponibles o
Las computadoras en ese momento eran muy nuevas pero capaces de tratar con
Operaciones bastante bien; Por otro lado, incluso hoy en día tareas como la visión y el sonido
Reconocimiento no son fácilmente programables sin el uso de frameworks especiales, no asi las operaciones y funciones matemáticas. Sin embargo, el cerebro puede realizar estas últimas tareas más eficientemente que las primeras, y este hecho
Realmente intriga a científicos e investigadores.

Por lo tanto, una [ANN](https://es.wikipedia.org/wiki/Red_neuronal_artificial) (Artificial Neural Newtwork) se supone que es una estructura para realizar tareas como el Reconocimiento de patrones, aprendiendo de datos, y en las tendencias de pronóstico, al igual que un experto puede hacer una base del conocimiento, en oposición al enfoque algorítmico convencional que
Requiere un conjunto de pasos a realizar para lograr un objetivo definido. Una ANN en su lugar tiene la capacidad de aprender a resolver alguna tarea por sí misma, debido a su alta estructura de red interconectada.

### El elemento mas básico : "Neurona Artificial"

Las neuronas naturales han demostrado ser procesadores de señales ya que reciben micro señales
En las dendritas que pueden desencadenar una señal en el axión dependiendo de su fuerza o
magnitud. Podemos entonces pensar en una neurona es como tener un colector de señal en las entradas
Y una unidad de activación en la salida que puede activar una señal que será reenviada A otras neuronas. Por lo tanto, podemos definir la estructura de la neurona artificial como se muestra en la Siguiente figura:


![](https://i.imgur.com/7tjpx2q.png)


### Dar vida a las neuronas: Funcion de Activacion


La salida de la neurona viene dada por una función de activación. Esta funcion añade
No linealidad al procesamiento de la red neuronal, que es necesario porque la neurona tiene conductas no lineales. Una función de activación suele estar limitada entre dos valores en la salida, siendo por lo tanto una función no lineal, pero en algunos
casos, puede ser una función lineal. 

Las cuatro funciones de activación más utilizadas son las siguientes:

* Sigmoide
* Tangente hiperbólica
* Umbral de limitación difícil
* Puramente lineal

![](https://i.imgur.com/Bwu1Qib.png)


### Los valores fundamentales - pesos

En las redes neuronales, los pesos representan las conexiones entre las neuronas y  la capacidad de "amplificar" o "atenuar" las señales neuronales (lo que una neurona "real" se logra por medio de impulsos electricos y bioquimicos), ya sea que los pesos por ejemplo, multipliquen las señales, dando asi que el valor de entrada original cambie. 

Siempre que las entradas (inputs) provienen de otras neuronas o del mundo externo(capa externa o primaria), los pesos se consideran una Conexione establecida de la red entre sus neuronas. 

Puesto que los pesos inputs de la red neuronal e influyen en sus resultados, es comun considerarlos como otro input mas de las redes neuronales.

![](https://i.imgur.com/wzdi0iJ.png)

.
### "bias" - Un parametro importante

La neurona artificial puede tener un componente independiente que añade una señal extra A la función de activación. Este componente se llama **bias** (valor de sesgo).

Al igual que las entradas, los sesgos también tienen un peso asociado. Esta función ayuda en la representación del conocimiento de redes neuronales como un sistema más puramente no lineal.



## Las partes que forman el todo (layers)


Las neuronas naturales se organizan en capas, cada capa (layer) proporcionando un nivel específico de tratamiento; Por ejemplo, la capa de entrada recibe estímulos directos desde el Mundo exterio (la "realidad") y las capas de salida activan acciones que tendrán una influencia directa en el mundo exterior. 

Entre estas capas, hay una serie de capas ocultas, en el sentido de que no interactúan directamente con el mundo exterior. En la neurona artificial todas las neuronas de una capa comparten las mismas entradas y la misma función Que se muestra en la siguiente figura.

![](https://i.imgur.com/5edtDMk.png))

Las redes neuronales pueden estar compuestas de varias capas vinculadas, formando los llamados
Redes multicapa. Las capas neurales se pueden dividir básicamente en tres clases:

* Capa de entrada
* Capa ocultaa
* Capa de salida

En la práctica, una capa neural adicional añade otro nivel de abstracción de la Fuera de los estímulos, aumentando así la capacidad de la red neural para representar más complejos conocimiento .


## Sobre Arquitecturas la red neuronal

Básicamente, una red neuronal puede tener diferentes diseños, dependiendo de cómo Neuronas o capas neuronales están conectadas entre sí. Cada red neuronal La arquitectura está diseñada para un fin específico. Las redes neuronales se pueden aplicar a
Número de problemas y, dependiendo de la naturaleza del problema, los Red debe ser diseñada con el fin de abordar este problema de manera más eficiente.

Básicamente, hay dos modalidades de arquitecturas para redes neuronales:

* Conexiones neuronales
	+ Redes monocapa
	+ Redes multicapa
* Flujo de señal
	+ Redes de feedforward
	+ Redes de retroalimentación
	
### Redes mono capa

En esta arquitectura, todas las neuronas se presentan en el mismo nivel, formando una sola, Como se muestra en la siguiente figura:

![](https://i.imgur.com/awSjDyr.png)

La red neuronal recibe las señales de entrada y las alimenta en las neuronas, que A su vez producen las señales de salida. Las neuronas pueden estar altamente conectadas a Otras con o sin recurrencia. Ejemplos de estas arquitecturas son la capa única
Perceptron, Adaline, mapa auto-organizativo, redes neurales de Elman y Hopfield.

## Redes multicapa

En esta categoría, las neuronas se dividen en múltiples capas, cada capa correspondiente A una distribución paralela de neuronas que comparte los mismos datos de entrada, como se muestra en el Siguiente figura:

![](https://i.imgur.com/Om9Ply7.png)

Las funciones de base radial y perceptrones multicapa son buenos ejemplos de esto
arquitectura. Estas redes son realmente útiles para aproximar datos reales a
Función especialmente diseñada para representar esos datos. Además, debido a que
Múltiples capas de procesamiento, estas redes están adaptadas para aprender de las
Datos, pudiendo separarlo o determinar más fácilmente el conocimiento que
Reproduce o reconoce estos datos.


## Redes de feedforward

El flujo de las señales en redes neuronales puede estar en una sola dirección o en
reaparición. En el primer caso, llamamos a la arquitectura de red neuronal feedforward,
Puesto que las señales de entrada son alimentadas a la capa de entrada; Después, después de ser procesado,
Son reenviados a la capa siguiente, tal como se muestra en la figura en la capa múltiple
sección. Los perceptrones multicapa y las funciones de base radial son también buenos ejemplos de
Redes de feedforward.


### Feedback networks

Cuando la red neuronal tiene algún tipo de recurrencia interna, significa que Las señales se retroalimentan en una neurona o capa que ya ha recibido y Procesado esa señal, la red es del tipo de retroalimentación. Vea el siguiente
Figura de redes de retroalimentación:

![](https://i.imgur.com/Dt0Lced.png)

La razón especial para añadir recurrencia en la red es la producción de una dinámica
Comportamiento, particularmente cuando la red soluciona problemas relacionados con
O reconocimiento de patrones, que requieren una memoria interna para reforzar el aprendizaje
proceso. Sin embargo, estas redes son particularmente difíciles de entrenar,
aprender. La mayoría de las redes de retroalimentación son de capa única, como Elman y Hopfield
Redes, pero es posible construir una red multicapa recurrente, como eco y
Recurrentes multicapas.

## De la ignorancia al proceso de aprendizaje del conocimiento

Las redes neuronales aprenden ajustando las conexiones entre las neuronas, a saber:
los pesos. Como se menciona en la sección de estructura neural, los pesos representan la
Conocimiento de redes neuronales. Diferentes pesos hacen que la red produzca
Resultados para las mismas entradas. Así, una red neuronal puede mejorar sus resultados adaptando
Sus pesos según una regla de aprendizaje. El esquema general del aprendizaje se representa en
La siguiente figura:

![](https://i.imgur.com/0WlQIgZ.png)

La figura anterior se llama aprendizaje supervisado porque Hay una salida deseada, pero las redes neurales pueden aprender sólo por los datos de entrada, Sin ninguna salida deseada (supervisión). Luego veremos Cómo aprenden las redes neuronales,
Vamos a profundizar en el proceso de aprendizaje de la red neuronal.


