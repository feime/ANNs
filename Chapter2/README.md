## Capítulo 2. Cómo aprenden las redes neuronales

El proceso  que realizan las redes neuronales para aprender
de los datos, Entrenamiento, prueba y validación que a diferencia de los
ordenadores digitales ordinarios que pueden ejecutar sólo aquellas tareas
a las que están programados, los sistemas neuronales pueden mejorar y realizar
nuevas actividades de acuerdo con algunos criterios de satisfacción.
En otras palabras, las redes neuronales no necesitan ser programadas;
Ellos aprenden el programa por sí mismos

* Proceso de aprendizaje
* Algoritmo de aprendizaje
* Tipos de aprendizaje
  + Supervisado
  + No supervisado

### Paradigmas de aprendizaje

Existen básicamente dos tipos de aprendizaje para las redes neuronales, es decir,
supervisado y sin supervisión. El aprendizaje en la mente humana, por ejemplo,
también funciona de esta manera. Podemos aprender de las observaciones sin
ningún tipo de patrón objetivo (sin supervisión), o podemos tener un maestro que
nos muestre el patrón correcto a seguir (supervisado). La diferencia entre estos
dos paradigmas se basa principalmente en la relevancia de un patrón objetivo y
varía de un problema a otro.

### Aprendizaje supervisado

Esta categoría de aprendizaje se relaciona en pares de X e Y, y el objetivo es
asignarlos en una función f: X → Y. Aquí, los datos Y son el supervisor, las
salidas deseadas de destino y los datos X son el origen- Datos independientes
que generan los datos Y. Es análogo a un maestro que está enseñando a alguien
una   determinada tarea a realizar:

Una característica particular de este paradigma de aprendizaje es que existe una
referencia de error directa, que es sólo la comparación entre el objetivo y el
resultado real actual. Los parámetros del sistema se introducen en una función de
coste, que cuantifica el desajuste entre las salidas deseadas y las reales.

Una función de coste es sólo una medida que se lleva a un problema de
optimización. Esto significa que uno busca encontrar los parámetros que llevan
la función de coste al valor más bajo posible.

### Aprendizaje sin supervisión

En el aprendizaje sin supervisión, tratamos sólo con datos sin etiquetado o
sin clasificación; Aqui nuestra estructura neuronal trata de extraer inferencias
y conocimiento teniendo en cuenta sólo los datos de entrada X.


Esto es análogo al autoaprendizaje, cuando alguien aprende por sí mismo teniendo
en cuenta su experiencia y un conjunto de criterios de apoyo. En el aprendizaje
sin supervisión, no tenemos un patrón deseado definido que se aplicará en cada
observación, pero la estructura neural puede producir uno por sí mismo sin
ninguna necesidad de supervisión.

![](https://snag.gy/eQbv0D.jpg)

### Algoritmo de estructuración - aprendizaje sistemático


Lo recomendable es que el proceso de aprendizaje debiera ser controlado, un
parametro important es el porcetaje de aprendizaje, comun mente representado por
la letra griega η.

Este parametro determina que tan fuerte pueden variar en la red neuronal
el hiper espacio de los pesos, Vamos a imaginar una ANN simple con dos entradas
a una sola neurona con una salida, por lo que tendriamos dos pesos w1 y w2
Ahora supongamos que queremos entrenar esta red e imaginar si podriamos evaluar
el error para cada par de pesos, supongamos que encontramos una superficie como
en la siguiente figura

![](https://snag.gy/do7U0F.jpg)

El parametro η es responsable de regular que tan cercanos estan los pesos de
moverese a la superficie, esto incrementaria la velocidad de aprendizaje pero
tambien puede empeorar al conjunto de los pesos de la iteracion previa.

Otro parametro importante es la condicion de paro usualmente el entrenamiento
para el entrenamiento cuando un error ocurre pero hay casos en los que la red
neuronal falla en aprender y hay un pequeño o no cambio en los valores de los
pesos, en estos casos un numero maximo de iteraciones o generacione es un buen
enfoque de condicion de paro.

### Medida de error y Funcion Costo

Es extremadamente importante para el exito del entrenamiento superviaso, vamos a
suponer que que le damos un conjunto de N registros que contiene pares de
valores X y T como variables, donde X son los valores de entrada independientes
y T soon los valores objetivo (target) dependientes de X vamos a conciderar
asi una funcion matematica ANN() que prodice Y de las salidas cuando son
suministrados los valores X.

y= ANN(x)

Para cada valor de x a la ANN este producira y que una vez comparado con el
valor target t nos daria el error

e=y-t

esto seria un valor de error para una medida individual, debenos tomar una medida
para el valor general de error de la red neuronal cubriendo todos pares de
datos N, vamos a medir el costo de este aprendizaje con la funcion C de costos

![](https://snag.gy/UfbQZ9.jpg)


Donde  X son las entradas, T  las salidas esperadas, W son los pesos, x[i] es
la entrada al instante i, t[i] es la salida esperada al instante i.

El resultado de la funcion es una medida sobre estimada del error entre las salidas
esperadas y las de la red nuronal en cada iteracion, y esta debera ser una funcion
a minimizar.


### Implementacion

Hasta ahora, hemos definido teóricamente el proceso de aprendizaje y cómo se
lleva a cabo. Sin embargo, en la práctica, nos debemos sumergir un poco más en la
lógica matemática, el algoritmo de aprendizaje en sí.

Un algoritmo de aprendizaje es un procedimiento que impulsa el proceso de
aprendizaje de las redes neuronales y está fuertemente determinado por la
arquitectura de la red neuronal. Desde el punto de vista matemático, se desea
encontrar los pesos óptimos W que pueden conducir la función de coste C (X, [Y])
al valor más bajo posible.


Al igual que cualquier programa que deseemos escribir, deberíamos haber definido
nuestro objetivo, aquí estamos hablando de una red neuronal para
aprender un poco de conocimiento. Debemos presentar este conocimiento
(o entorno) a la ANN y comprobar su respuesta, que naturalmente no tendrá
sentido. La respuesta de la red se compara entonces con el resultado esperado,
y ésta retro alimenta a una función de coste C. Esta función de coste determinará
cómo se pueden actualizar los pesos W.

El algoritmo de aprendizaje calcula entonces el término ΔW, que significa la
variación de los valores de los pesos a añadir. Los pesos se actualizan:

![](https://snag.gy/SPIh6w.jpg)


Donde k se refiere a la k-ésima iteración y W (k) se refiere a los pesos
neuronales en la k-ésima iteración, y posteriormente, k + 1 se refiere a la
siguiente iteración.

A medida que se ejecuta el proceso de aprendizaje, la red neural debe dar
resultados cada vez más cercanos a la expectativa, hasta que finalmente alcanza
los criterios de aceptación. El proceso de aprendizaje se considera entonces
finalizado.

* Entrenamiento, prueba y validación
* Medidas de error
* Generalización

El proceso de aprendizaje que hemos cubierto se llama entrenamiento. Después de
entrenar una red neuronal, deberíamos probarla si realmente ha aprendido. Para
la prueba, debemos presentar a la red neuronal otra fracción de datos del mismo
entorno que ha aprendido. Esto es necesario porque, al igual que el estudiante,
la red neural podría responder correctamente con sólo los puntos de datos a los
que se había expuesto; Esto se llama sobreentrenamiento. Para comprobar si la
red neuronal no ha pasado el sobreentrenamiento, debemos comprobar su
respuesta a otros puntos de datos.

La figura siguiente ilustra el problema del sobreentrenamiento. Imagine que
nuestra red está diseñada para aproximar alguna función f (x) cuya definición
es desconocida. La red neural fue alimentada con algunos datos de esa función y
produjo el siguiente resultado que se muestra en la figura de la izquierda.
Sin embargo, al expandirse a un dominio más amplio, observamos que la respuesta
neural no sigue los datos.

![](https://snag.gy/VRI1yL.jpg)

En este caso, vemos que la red neuronal no pudo aprender todo el entorno
(la función f (x)). Esto sucede por varias razones:

* La red neuronal no recibió suficiente información del entorno
* Los datos del entorno son no deterministas
* Los conjuntos de datos de capacitación y pruebas están mal definidos
* La red neuronal ha aprendido mucho de los datos de entrenamiento y se olvida de los datos de las pruebas



### Perceptron

Los perceptrones aprenden tomando unicamente en cuenta
el error entre los valores objetivo (target) y las salidas en cada
iteracion y la estimacion de aprendizaje

La regla de actulizacion entre iteraciones es la siguiente:

![](https://snag.gy/QY8kbi.jpg)

Donde W i es el peso de la i-ésima entrada de la neurona,
t[k] es la salida objetivo de la k-ésima muestra, Y[k] es el resultado
de la red neuronal para la k-ésima muestra, Xi[k] es la i-ésima
entrada para la k-ésima muestra, y η es la tasa de aprendizaje.

Se puede observar que esta regla es muy simplista y no considera
las no linealidades perceptrónicas presentes en la función de activación;
Simplemente va en la dirección  opuesta del error en la ingenua esperanza
de que esto llevaría a la red cerca del objetivo.

### Regla Delta

Un mejor algoritmo se desarrolló basado en el gradiente decendiente para
considerar la no linealidad, así como su derivada.

Lo que este algoritmo tiene además de la regla de perceptrón es la derivada
de la función de activación g´(h), siendo h la suma ponderada de todas las
entradas de las neuronas antes de pasarlas a la función de activación.
Por lo tanto, la regla de actualización es la siguiente:

![](https://snag.gy/fG3c8u.jpg)

La enterior es conocida como neurona *adaline*

### Practica 2

La clase NeuralNet presentada en la practica anterior se ha actualizado para
incluir el dataset de entrenamiento (entrada y salida esperada *target*),
parámetros de aprendizaje y ajustes de la función de activación. La función
InputLayer también se actualizó para incluir un método. Añadimos al proyecto
las clases *Adaline*, *Perceptron* y *Training*.

Dos enumeraciones se crearon para definir los tipos de ANNs

 ```java
TrainingTypesENUM
 ```


La otra enumeracion que se utiliza es para definir el tipo de funcion de activacion

 ```java
ActivationFncENUM
 ```

Adiocional a estos parametros vamos a definir variables que representen
la condicion de paro, erro MSE,  y el numero de generacion

 ```java
 private int epochs;
 private double error;
 private double mse;
 ```

La estimacion de aprendizaje (learning rate) ha sido definido en la clase
NeuralNet, necesitamos un metodo que actualize los peso  de las neuronas,
vamos a ver  el metodo CalcNewWeight.

```java
private double calcNewWeight(TrainingTypesENUM trainType,
      double inputWeightOld, NeuralNet n, double error,
      double trainSample, double netValue) {
    switch (trainType) {
    case PERCEPTRON:
      return inputWeightOld + n.getLearningRate() * error * trainSample;
    case ADALINE:
      return inputWeightOld + n.getLearningRate() * error * trainSample
          * derivativeActivationFnc(n.getActivationFnc(), netValue);
    default:
      throw new IllegalArgumentException(trainType
          + " does not exist in TrainingTypesENUM");
    }
  }
```

### Implementacion de red  con Perceptrons (warning system)

Para facilitar la explicacion con los perceptrones vamos a conciderar un sistema
de alertas, su funcionalidad esta basada en la logica de una compuerta logica
**AND** hay dos sensores y las reglas para las alertas son:

* Si ambas o alguna esta desabilitada el warning es disparado
* Si ambas estan habilitadas la alerta no es disparada

![](https://snag.gy/Dq2dLB.jpg)

Para codificar el problema vamos a representar con 0 deshabilitado 1 significara
habillitado, de tal forma que las entradas posibles al sistema de alertas es.

![](https://snag.gy/EO13aH.jpg)

```java
private void testPerceptron() {
  NeuralNet testNet = new NeuralNet();

  testNet = testNet.initNet(2, 0, 0, 1);
  ...
```
