# Definición de _Structs_

Una vez entendida la declaración de un `struct` vamos a ver las diferentes formas de declarar o definir tipos de estructuras.

## Declaración de variables estructuradas

A la versión para declarar variables que hemos visto en la página anterior se le suman dos posibilidades más:

* Directamente en la definición:
  ```cpp
  struct nombre {
    tipo_miembro_1 nombre_miembro1;
    tipo_miembro_2 nombre_miembro2;
    tipo_miembro_3 nombre_miembro3;
    ...
  } var1, var2, var3,...;
  ```
* Tras la definición:
  ```cpp
  struct nombre {
    tipo_miembro_1 nombre_miembro1;
    tipo_miembro_2 nombre_miembro2;
    tipo_miembro_3 nombre_miembro3;
    ...
  };
  
  struct nombre var1, var2, var3, ... ;
  ```

## Definición de nuevos tipos

Usando la sentencia _typedef_. Su uso con los structs es el siguiente:
```cpp
typedef struct{
  tipo_miembro_1 nombre_miembro1;
  tipo_miembro_2 nombre_miembro2;
  tipo_miembro_3 nombre_miembro3;
} nombre;

nombre var1, var2, var3, ... ;
```
