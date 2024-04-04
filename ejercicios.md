# Análisis de datos con Numpy, Panda y Matplotlib

# ¿Qué es Data Analysis o el Análisis de datos?

Es el proceso de inspección, limpieza de datos, transformación de datos con el objetivo de descubrir datos útiles y
ayude al soporte de toma de decisiones.

# ¿Qué pasos tenemos que dar para realizar un análisis exploratorio de datos?

1. Transformar los datos como llegan al formato que necesito
2. Limpieza de datos (preprocesado de la información)
3. Visualización de los datos
4. Preparar el modelo de datos
5. Realizar un análisis aprendizaje automático

# Numpy. Pero ¿Qué es Numpy?

Numpy, es un paquete para realizar computación científica y operaciones y cálculos.

## Estructuras Array Numpy

#### Ejercicio 1: Crea un array de una dimensión. (Vector)

```python
vector = np.arange(7)
```

#### Ejercicio 2: Crea un array de dos dimensiones. (Array)

```python
matriz = np.arange (4).reshape(2,2)
```

#### Ejercicio 3: Crea un vector y un array a partir de la siguiente lista
[1,11,111,1111]

*pista tienes que crear una lista y utilizar np.array()*

``` python
lista = [1, 11, 111, 1111]
vector = np.array(lista)
array = np.array(lista)
```

#### Ejercicio 4: Crea un array 5x5 de zeros
``` python
array_zeros = np.zeros((5, 5))
```

#### Ejercicio 5: Crea un vector cuyo límite inferior sea 0 y el límite superior sea 20 y tenga 5 elementos comprendidos en ese intervalo que sean liealmente iguales

 ```python
vector = np.linspace(0, 20, 5)
```

#### Ejercicio 6: Crea un array de 8 elementos de 2x2x2 de ceros (Tensor)

```python
tensor = np.zeros((8, 2, 2, 2))
```

####  Ejercicio 7: Crea un array que vaya de 2 al 20 y obten el elememnto de la posición 7


```python
array = np.arange(2, 21)
elemento_posicion_7 = array[6]
```

#### Ejercicio 8: crea un vector de 20 elementos y mediante el método slice() crea otro vector a partir del vector de 20 elementos que empiece en 1, termine en 10 y tenga los números de dos en dos

``` python
vector_20 = list(range(1, 21)) 
vector_slice = vector_20[0:10:2]
```

#### Ejercicio 9: Explica el siguiente código:

``` python
arr7 = np.arange(20)
print(arr7[2:])
```
Escribe aquí tu explicación: La función np.arange() devuelve un array de valores que comienza desde 0 y termina en el número especificado menos uno. En este caso, devuelve un array que va desde 0 hasta 19. Luego, se utiliza el slicing para acceder a una porción del array. La notación arr7[2:] indica que queremos seleccionar todos los elementos del array arr7 empezando desde el índice 2 hasta el final del array. El índice 2 corresponde al tercer elemento del array, ya que los índices en Python y NumPy comienzan desde 0. Entonces, arr7[2:] devuelve todos los elementos del array arr7 desde el tercer elemento (índice 2) hasta el último elemento


#### Ejercicio 10: Utilizando lo anterior a partir del arr7 quiero obtener una lista que va de 0 a 15

``` python
arr7 = np.arange(20)  
subarray = arr7[:16]
lista_0_15 = subarray.tolist()
```
#### Ejercicio 11: Crea un array de ceros de 3x3. A partir de ese array prueba el atributo shape, ndim, y itemsize. Explica que nos dicen estos atributos sobre la estructura

``` python
array_zeros = np.zeros((3, 3))
print("Array de ceros de 3x3:")
print("\nAtributo shape:", array_zeros.shape)
print("Atributo ndim:", array_zeros.ndim)
print("Atributo itemsize:", array_zeros.itemsize)
```
'''-shape: El atributo shape devuelve una tupla que indica las dimensiones del array. En este caso, el array tiene una forma de (3, 3), lo que significa que tiene 3 filas y 3 columnas.

-ndim: El atributo ndim devuelve el número de dimensiones del array. En este caso, el array es bidimensional, por lo que ndim devolverá 2.

-itemsize: El atributo itemsize devuelve el tamaño en bytes de cada elemento del array. Dado que estamos trabajando con un array de ceros de tipo float64 (por defecto en NumPy), cada elemento tiene un tamaño de 8 bytes (64 bits).'''


# LEER Y ESCRIBIR EN FICHEROS

descarga el siguiente fichero que es una base de datos de huracanes

https://github.com/rmcelreath/rethinking/blob/master/data/Hurricanes.csv

```python
arr_csv = np.genfromtxt('./Hurricanes.csv', delimiter = ',')
np.savetxt('newfilex.csv', arr_csv, delimiter = ',')
```

Explcia que hace este código

