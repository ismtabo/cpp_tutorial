# _Arrays_ multidimensionales

Hasta ahora hemos visto los _arrays_ para almacenar colecciones de datos del mismo tipo sobre direcciones de memorias conjuntas. Llevado al terreno de las matemáticas obtendremos vectores de una dimensión. La pregunta ahora es si este método puede ampliarse a más de una dimesión. Veamos en un principio como podemos tener _arrays_ de _arrays_ ó _arrays_ de dos dimensiones.

```cpp
int matrix[][];
```

Al igual que con los _arrays_ unidimensionales para añadir una dimensión más, añadimos un nivel de corchetes, indicando que vamos a tener un _array_ de _arrays_. De tal manera que podríamos definir una matriz de enteros de 2 filas, y 3 columnas como:
```cpp
int matrix[2][3];
```

Se puede observar como la primera dimensión podemos tomarlo como las dimensión de las filas, y la segunda como el de las columnas; pues es así como luego se almacenará en la memoria. Ver más al respecto en [Row- and column-major order](https://en.wikipedia.org/wiki/Row-_and_column-major_order).

## Inicialización

Como hemos visto la definición de una matriz de dos dimensiones se asemeja a la de una; de la misma manera la inicialización es parecida, teniendo ciertas modificaciones. Vemos las distintas alternativas:

```cpp
int matrix[2][3] = {1,2,3,4,5,6};
int matrix[2][3] = {{1,2,3}, {4,5,6}};
```

Al almacenarse en direcciones de memoria conjuntas, podemos inicializar de la misma manera que haríamos con un _array_ con el mismo número de elementos (2*3=6 elementos). También podemos inicializar fila por fila.

**Aviso**: Hay que tener cuidado con los valores de cada dimensión, debido a en caso de inicializar una fila con más elementos de los que acepta el _array_ bidimensional, causaría un fallo de compilación.

## Acceso a elementos

Veamos como podemos acceder a los elementos ante _arrays_ de más de una dimensión. Como en el caso de una dimensión, el nombre del _array_ multidimensional es un puntero, pero no a un elemento del tipo del _array_, sino un puntero al primer array. El cual al ser un puntero a su primer elemento, podemos extraer las siguientes igualdades:
```
matrix == matrix[0] == &matrix[0][0]
```

Para acceder un valor que se encuentre en la fila `i` y columna `j` --elemento de coordenadas (`i`, `j`)-- utilizaremos la siguiente expresión:
```cpp
matrix[i][j]
```

## _Arrays_ multidimensionales y referencias

Al igual que con los _arrays_ de una dimensión, las referencias no cambian su comportamiento. Se utilizan de igual manera, teniendo cuidado de tener el mismo tipo que el array multidimensional al que se quiere referenciar.

## _Arrays_ multidimensionales y punteros

Si los _arrays_ unidimensionales estaban relacionados con los punteros, como podemos relacionarlos cuando tienen más de una dimensión. Primero tenemos que plantearnos que produciría el siguiente código:
```
int matrix[2][3]= {{1,2,3}, {4,5,6}};
int *ptr = matrix;
```

Como hemos visto, `matrix` es un puntero al primer _array_(primera fila), por lo que el compilador nos avisará que los tipos `int (*)[3]` de `matrix` y el de `int *` de `prt` son incompatibles. Por lo tanto el código correcto sería:
```cpp
int matrix[2][3]= {{1,2,3}, {4,5,6}};
int (*ptr)[3] = matrix;
```

Pero cuidado, el puntero `ptr` nos servirá para navegar entre las filas, ya que es un puntero a _arrays_ de enteros de tamaño tres, de tal manera que cuando incrementemos el valor del puntero con `ptr++` la dirección de memoria a la que apunta incrementará 12 bytes (tamaño del tipo `int[3]`), saltando a la dirección de la siguiente fila. Por lo que el acceso desde punteros a elementos se deberá hacer mediante:
```cpp
int *elemptr = *ptr;
cout << *elemptr << endl;       // Element [0][0]
cout << *(elemptr + 2) << endl; // Element [0][2]
ptr++;
elemptr = *ptr;
cout << *elemptr << endl;       // Element [1][0]
cout << *(elemptr + 2) << endl; // Element [1][2]
```

**Aviso**: como se puede observar, al declarar el puntero `ptr` se debe incluir `* ptr` entre paréntesis ya que el operador `[·]` tiene mayor precedencia.

## _Arrays_ multidimensionales y funciones

Por último, para pasar estos _arrays_ de _arrays_ como parámetros de una función, lo haremos de una manera muy similar a la vista para _arrays_ de una dimensión, teniendo cuidado con definir correctamente los tamaños de cada dimensión del array, y en el caso de utilizar punteros, tener especial cuidado con lo visto en el apartado anterior. Las formas de declarar como parámetro serán: 

**Mediante un puntero:**
```cpp
void method(int (*)[size_of_2nd_dim]);
```

**Mediante tamaño indefinido de alguna dimensión:**
```cpp
void method(int [][size_of_2nd_dim]);
```

**Mediante tamaños definidos de cada dimensión:**
```cpp
void method(int [size_of_1st_dim][size_of_2nd_dim]);
```

## Más de dos dimensiones

Lo visto es escalable a 3 o más dimensiones, teniendo especial cuidado en los siguientes detalles:
- El nombre del _array_ multidimensional será un **puntero** al primer elemento de la siguiente dimensión.
- Los _arrays_ son punteros a la dirección de memoria del primer elemento de la colección.
- Los **punteros** utilizados deben ser del **mismo tipo**, tener las **mismas dimensiones** y tener el mismo **tamaño de cada dimensión** que a lo que se quiere apuntar. A excepción de la primera, la cual la identificamos con `(*)`. Es decir: 
Array: `int[1][2][3]` Punteros:
    - Primera dimensión: `int(*)[2][3]`
    - Segunda dimensión: `int(*)[3]`
    - Tercera dimensión(elemento final): `int*`
