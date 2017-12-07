# Definición de _Structs_

Una vez entendida la declaración de un `struct` vamos a ver las diferentes formas de declarar o definir tipos de estructuras.

## Declaración de variables estructuradas

A la versión para declarar variables que hemos visto en la página anterior se le suman dos posibilidades más:

* Directamente en la definición:
  ```cpp
  struct name {
    type_member_1 member1;
    type_member_2 member2;
    type_member_3 member3;
    ...
  } var1, var2, var3,...;
  ```
* Tras la definición:
  ```cpp
  struct name {
    type_member_1 member1;
    type_member_2 member2;
    type_member_3 member3;
    ...
  };
  
  struct name var1, var2, var3, ... ;
  ```

## Definición de nuevos tipos

En **C**, para usar **structs** como tipo de parámetros y variables en todo el código, es necesario declararlo como tipo. En **C++** en cambio no es obligatorio. Para definir una estructura usando la sentencia _typedef_, el ejemplo es el siguiente:
 
```cpp
typedef struct{
  type_member_1 member1;
  type_member_2 member2;
  type_member_3 member3;
} name_t;

name_t var1, var2, var3, ... ;
```

**Consejo**: por convención, en **C/C++** se suelen nombrar a los nuevos tipos definidos (**structs** o tipos creados mediante `typedef`) con la primera con mayúscula y terminando el nombre con `_t`, como `Complex_t`, para indicar que es un tipo. Más sobre convenciones de programación en: [Naming convention](https://en.wikipedia.org/wiki/Naming_convention_\(programming\))
