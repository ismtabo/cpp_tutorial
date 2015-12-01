Operador coma, casting y _size_
====

Operador coma
----

El operador _coma_ nos permite dentro de una asignación, realizar un conjunto de operaciones que se encuentran entre paréntesis y devolver la última, sabiendo que se operan de izquierda a derecha. Veamoslo con un ejemplo:

`a = (b=3, b+2);`

En la anterior línea de código se realizan un conjunto de operaciones. Primero asignamos el valor 3 a la variable `b`, al valor de esa variable le sumamos dos, finalmente, el valor calculado por `b+2` es asignado a la variable `a`.

Es decir, es equivalente a:

```cpp
b = 3;
a = b+2;
```

Casting
----

Algo que nos va a interesar a la hora de codificar **C++** es como pasar de un tipo de variables a otras. Como en otros lenguajes, lo haremos mediante un _casting_. Esta característica se ha heredado de **C** por lo que el código es similar.

```cpp
int i;
float f = 3.14;
i = (int) f;
```

También se puede hacer casting mediante notación de funciones:

```cpp
i = int(f);
```

**Aviso**: no todos los tipos/clases se pueden pasar a ser otro tipo/clases. Casos como:
```cpp
int i;
string s = "1344";
i = (int)s;
```
Para ello existen funciones especiales. En este caso para pasar de _string_ a _int_ existe la función `std::stoi()`, que convertirá una cadena en un entero, si es posible.

_size_
----

Este operador acepta un único parámetro, que puede ser un tipo o una variable, y devuelve el tamaño en _bytes_(B) del tipo o variable:
```cpp
x = sizeof (char);
```
En este caso el valor asignado a `x` será 1, ya que un tipo _char_ ocupa un _byte_.

Este operador se ejecuta en tiempo de compilación, por lo tanto en tiempo de ejecución el valor ya está determinado.

En el bloque anterior de tipos de datos, puedes encontrar una tabla con los tamaños de cada tipo básico.