### Laboratorio 1

La primer red neuronal presentada un ejemplo sencillo  de "Elementos"
de una red neuronal, como tal no es realmente ningun algoritmo
de aprendizaje, solo es un un bosquejo muy sencillo de los Elementos
y la conjugacion de los conceptos de neurona, capa de entrada,
capa escondida y capa de salida, asi como de los conceptos mas
simples y fundamentales de la POO.


La clase que tiene el metodo main de esta practica es NeuralNetTest.java

```java
public class NeuralNetTest {
  public static void main(String[] args) {
    NeuralNet n = new NeuralNet();
    n.initNet();
    n.printNet();

  }
}
```

NeuralNet es una clase con

* Una capa de neuronas "inputLayer"
* Dos capas de neuronas "hiddenLayer"
* Una capa de neuronas "outputLayer"

```java
public class NeuralNet {

	private InputLayer inputLayer;
	private HiddenLayer hiddenLayer;
	private ArrayList<HiddenLayer> listOfHiddenLayer;
	private OutputLayer outputLayer;
	private int numberOfHiddenLayers;
...

}
```

La representacion de este bosquejo seria el siguiente diagrama de clases
en lenguaje unificado de modelado, UML:


![](https://snag.gy/ys8SDm.jpg)

La salida es un sencillo reporte por cada capa de sus salidas
aqui aun no hablamos de funciones, parametros de aprendizaje, si no hasta
la siguiente practica.

![](https://snag.gy/S8cB0o.jpg)
