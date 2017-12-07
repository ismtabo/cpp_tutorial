# Uso de referencias

Como hemos visto, las **referencias** nos permiten tener _alias_ o enlaces de escritura/lectura sobre una misma dirección de memoria. Esto nos permite modificar y leer dicha dirección de memoria sin tener la variable en sí. 

En la sección de los bucles `for-in` y en la de funciones, se citan las referencias para poder mutar el contenido del iterador o de un parámetro, respectivamente. Veamos unos ejemplos:

## for-in

En el bucle `for-in` el uso de una referencia como iterador permite actualizar el elemento al que estemos referenciando en esa iteración. Como en :

``` cpp
for(int& n : numbers)
    n++;
```

Donde los valores de la lista `numbers` son incrementados en uno.

## Parámetros por referencia

Para pasar parámetros por referencia. Se pueden utilizar punteros, como veremos más adelante. O el operador `&`. Como se puede observar en la siguiente implementación de la función para intercambiar los valores de dos variables.

```cpp
void swap(int &a, int &b) {
  int tmp;
  tmp = a;
  a = b;
  b = tmp;
}
```

En este caso, al tener por referencia los parámetros `a` y `b`, los cambios que se hagan de estos en la función, tendrán efecto sobre las variables que se pasen como parámetros en la llamada de `swap`. Veamos un ejemplo:

```cpp
int a = 0, b = 1;
cout << a << " " << b << endl; // Prints: 0 1
swap(a, b);
cout << a << " " << b << endl; // Prints: 1 0
```
