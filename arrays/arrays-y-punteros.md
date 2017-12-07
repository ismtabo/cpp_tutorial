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

- **Asignación**: `int *ptr = array;`
- **Valor guardado en una dirección**: `*(ptr)`
- **Dirección del puntero**: `&(ptr)`
- **Incremento del puntero**: `ptr++`
- **Resta**: `int *ptr2 = array; cout << ptr - ptr2`
