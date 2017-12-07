# _Structs_ de _Structs_

Por último, los _structs_ permiten también agrupar miembros que sean a su vez _structs_. Pongamos el siguiente ejemplo.

Una lista enlazada, es una estructura de datos donde cada elemento de la lista está conectado al siguiente, de tal manera, que para recorrerla, deberemos empezar por el primer elemento hasta que ya no queden más. La siguiente estructura expondría los miembros que tendría que tener un _struct_ que represente un elemento.

```cpp
struct Element_t {
    int value;
    Element_t *next;
};
```

También podríamos representar la estructura lista como un grupo de punteros al primer, y al último elemento.

```cpp
struct LinkedList_t {
    Element_t *first;
    Element_t *last;
};
```

Ejercicio
---
- En las listas doble enlazadas cada elemento tiene acceso a su precedesor y al siguiente, implemente una estructura que represente dicho elemento.
