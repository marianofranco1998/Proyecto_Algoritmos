# Estructuras de Datos Avanzadas: Comparación de Algoritmos de Ordenamiento

Este proyecto consiste en un Jupyter Notebook con implementación en Python de seis algoritmos de ordenamiento distintos. Al ejecutar el código se generan varias gráficas de línea que se pueden utilizar para evaluar la eficiencia de los algoritmos de programación.

## Contenido
* [¿Qué es un algoritmo de ordenamiento?](#1)
* [¿Cuáles algoritmos de ordenamiento fueron evaluados?](#2)
* [¿Qué hace que un algoritmo sea eficiente?](#3)
* [¿Importa el orden en el cuál el algoritmo recibe los datos?](#4)
* [¿Importa la cantidad de datos que recibe el algoritmo?](#5)
* [¿Qué datos se utilizaron?](#6)
* [¿Cuál fue la metodología?](#7)
* [¿Cuáles fueron los resultados?](#8)
* [¿Qué se entrego?](#9)

## ¿Qué es un algoritmo de ordenamiento? <a name="1"></a>

Una algoritmo de ordenamiento se utiliza para reorganizar un [arreglo](https://es.wikipedia.org/wiki/Vector_(inform%C3%A1tica)) de datos/elementos de acuerdo a un criterio de comparación. Un criterio de comparación es esencialmente una [función](https://es.wikipedia.org/wiki/Funci%C3%B3n_matem%C3%A1tica#:~:text=La%20definici%C3%B3n%20general%20de%20funci%C3%B3n,un%20%C3%BAnico%20elemento%20de%20B.) que dada un dato/elemento, regresa un valor numérico. Un algoritmo de ordenamiento reordena un arreglo de datos/elementos, colocando los datos/elementos en un arreglo nuevo en orden ascendiente de acuerdo al criterio de comparación.

[Leer GeeksforGeeks para obtener más información.](https://www.geeksforgeeks.org/sorting-algorithms/)

## ¿Cuáles algoritmos de ordenamiento fueron evaluados? <a name="2"></a>

Dentro de este proyecto se evaluaron seis algoritmos diferentes. No es indispensable entender las diferencias entre ellos, pero si uno desea aprender más puede presionar el enlace en el nombre de cada algoritmo. Los algoritmos son los siguientes:

1. [Selection Sort](https://www.geeksforgeeks.org/selection-sort/)
2. [Insertion Sort](https://www.geeksforgeeks.org/insertion-sort/)
3. [Bubble Sort](https://www.geeksforgeeks.org/bubble-sort/)
4. [Merge Sort](https://www.geeksforgeeks.org/merge-sort/)
5. Mixcoac Sort (Variación de Merge Sort)
6. [Quick Sort](https://www.geeksforgeeks.org/quick-sort/)

## ¿Qué hace que un algoritmo sea eficiente? <a name="3"></a>

Hay dos métricas que podemos utilizar para determinar la eficiencia de un algoritmo: tiempo tardado y número de comparaciones.
1. **Número de Comparaciones:** Esto se refiere a la cantidad de veces que el algoritmo evalua una operación [booleana](https://es.wikipedia.org/wiki/Funci%C3%B3n_booleana), la mayoría de las veces esto ocurre dentro de una [estructura de control](https://es.wikipedia.org/wiki/Estructuras_de_control) simple (`if-else`) o dentro de la condición asignada de un [bucle](https://es.wikipedia.org/wiki/Bucle_(programaci%C3%B3n)#:~:text=Un%20bucle%20o%20ciclo%2C%20en,y%20el%20bucle%20do%2Dwhile.) (`for`, `while`).
2. **Tiempo Tardado:** Esto simplemente se refiere a la cantidad de tiempo (en segundos) que el algoritmo tarda en reordenar los datos que recibe.

## ¿Importa el orden en el cuál el algoritmo recibe los datos? <a name="4"></a>

El orden en el cuál el algoritmo recibe los datos es muy importante. Algunos algoritmos tienen ventaja si reciben sus datos ordenados, mientras que otros muestran mejor desempeño con datos más mezclados. Debido a esto, evaluamos el desempeño de cada algoritmo con tres tipos de ordenes inciales de los datos:

1. Ordenado
2. Orden Inverso
3. Orden Aleatorio

## ¿Importa la cantidad de datos que recibe el algoritmo? <a name="5"></a>

La cantidad de datos que recibe el algoritmo también es muy importante. Algunos algoritmos son muy eficientes con una pequeña cantidad pero se alentan mucho cuando reciben muchos datos. Por otro lado, hay algunos algoritmos que tienen mejor desempeño con muchos datos pero tienen un mal desempeño comparativo con cantidades de datos pequeñas. Por lo tanto, cada prueba se llevo a cabo con arreglos de datos de cinco distintos tamaños:

1. 100
2. 1000 
3. 2500 
4. 5000 
5. 10000

## ¿Qué datos se utilizaron? <a name="6"></a>

Para probar los algoritmos se utilizó el archivo `movie_titles.txt`, una lista del nombre, el código, y la fecha de estreno de más de 10000 películas. Se creo un [objeto](https://es.wikipedia.org/wiki/Objeto_(programaci%C3%B3n)) `Movie` con tres atributos: `nombre`,`codigo`, y `año`. Se selecciono el valor [ASCII](https://es.wikipedia.org/wiki/ASCII) de `nombre` como el criterio de comparación para el objeto.

## ¿Cuál fue la metodología? <a name="7"></a>

Cada prueba consistió en correr un algoritmo con una selección de datos específica, contando el tiempo para completar y el número de operaciones.

Se llevaron a cabo 72 pruebas en total, variando tres factores distintos: orden de los datos, número de datos, y algoritmo utilizado. El siguiente árbol ilustra esto:

![alt text](https://github.com/marianofranco1998/Proyecto_Algoritmos/blob/master/images/Decision_Tree_1.png "Diagrama")

Para los datos en orden aleatorio, se registro como prueba el promedio de número de comparaciones y tiempo tardado de 30 pruebas consecutivas. Esto se hizo para obtener una expectativa razonable de estos dos valores. Hacer solamente una prueba con datos aleatorios resultaría en gráficas muy distintas cada vez que se corre el Jupyter Notebook.

## ¿Cuáles fueron los resultados? <a name="8"></a>

Al final se produjeron seis gráficas, todas con el número de datos como el eje x. Tres de estas tenían número de comparaciones en el eje y y tres tenían en el eje y. Dentro de cada gráfica se crearon seis subgráficas, una para cada uno de los algoritmos de ordenamiento diferentes. El Jupyter Notbook produjo las siguientes gráficas.

### Eje-Y: Número de Comparaciones
<p float="left">
  <img src="https://github.com/marianofranco1998/Proyecto_Algoritmos/blob/master/images/A1.png" width="472" />
  <img src="https://github.com/marianofranco1998/Proyecto_Algoritmos/blob/master/images/A2.png" width="472" /> 
  <img src="https://github.com/marianofranco1998/Proyecto_Algoritmos/blob/master/images/A3.png" width="472" />
</p>

### Eje-Y: Tiempo Tardado
<p float="left">
  <img src="https://github.com/marianofranco1998/Proyecto_Algoritmos/blob/master/images/B1.png" width="472" />
  <img src="https://github.com/marianofranco1998/Proyecto_Algoritmos/blob/master/images/B2.png" width="472" /> 
  <img src="https://github.com/marianofranco1998/Proyecto_Algoritmos/blob/master/images/B3.png" width="472" />
</p>

## ¿Qué se entrego? <a name="9"></a>
[Este reporte](https://docs.google.com/document/d/1AarI4mo9nCETtxMMcOIzXVIFglF7Dm8Lc7BkU_PTyoc/edit?usp=sharing) se entrego después de la terminación del proyecto.
