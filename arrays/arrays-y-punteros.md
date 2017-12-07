# Arrays y punteros

Los arrays y punteros tiene mucho en común, de cara al compilador, ambos son punteros a direcciones de memoria. Ahora vamos a analizar las diferencias y semejanzas entre estas dos funcionalidades y como están relacionadas entre sí. Pongamos el ejemplo de un _array_ de enteros unidimensional:
```cpp
int array[3], *ptr;
```

El nombre del array es un puntero al primer elemento que contiene. Lo que hace que se cumpla la siguiente comparación:

```
array == &array[0]
```

Por lo tanto si asignamos:
```cpp
ptr = array;
```

Tendremos las siguiente igualdades:
```cpp
ptr == &array[0]
*ptr == array[0]
```

Es decir, podremos acceder al primer elemento mediante el operador `*` de los punteros. Es más, también tenemos acceso al resto de elementos del _array_ mediante la conocida _aritmética de punteros_(que explicaremos más adelante):
```cpp
*(ptr + 1) == array[1]
*(ptr + 2) == array[2]
```

Deducimos entonces que si tenemos un puntero a un _array_ de _n_ elementos podemos acceder al elemento _i_ con el puntero mediante la expresión:
```
*(ptr + i) == array[i]
```

Siempre y cuando se cumpla `0 <= i < n`, y nos salgamos del _array_ accediendo a una dirección de memoria incorrecta.


## Aritmética de punteros

Las bases que hacen posible ese acceso desde el puntero a los elementos del _array_ se conoce como aritmética de punteros y consta de cuatro operaciones básicas:

- **Asignación**: como su nombre indica, asignar al puntero una dirección de memoria: `int *ptr = array;`
- **Valor guardado en una dirección**: como vimos en la pasada sección, este operador devuelve el valor de la dirección del puntero: `*(ptr)`
- **Dirección del puntero**: valor de la dirección de memoria donde está guardado el puntero, no confundir con la dirección a la que apunta:  `&(ptr)`
- **Incremento del puntero**: al incrementar o decrementar el valor, la dirección que contiene el puntero variará según el tipo de este, al sumarse o restarse tantos bytes como correspondan al tipo: `ptr++` Es decir, en un puntero a entero, la unidad por la que se incrementa o decrementa son 4 (bytes).
- **Resta**: diferencia numérica entre dos direcciones de memoria, el resultado al igual que con la operación anterior se mide según el tipo del puntero: `int *ptr2 = array; cout << ptr - ptr2` Esta operación nos sirve de ayuda al poder calcular el tamaño de un array, calculando la diferencia entre los punteros al último y al primer elemento.

## Recorrer _array_ con punteros

A continuación ponemos el ejemplo de recorrer un array no con índices sino con punteros:

```cpp
int array[5] = {1,2,3,4,5};
int *ptr;

for(ptr = array; (ptr-array) < 5; ++ptr)
    cout << *ptr << " ";
cout << endl;
```

Ejercicio
---
- Modificar el último ejemplo para imprimir por pantalla los elementos del array pero desde el final al principio.
