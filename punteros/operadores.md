# Operadores
Existen dos operadores especiales relacionados con punteros:
- El operador "**&**"(dirección de): devuelve la dirección de memoria donde está asignada una determinada variable:.
```c
int *i,j;
j=5;
i=&j;//asignamos a i la dirección de j
```
- El operador "__*__": asociado a un puntero devuelve el valor de contenido en la dirección de memoria a la que apunta el puntero.
```cpp
cout << "Dirección de j en hexadecimal: 0x"<< hex<< i <<`\n`;
// accediendo mediante la dirección
cout << "Valor de j: "<< *i <<`\n`;
// accediendo mediante la variable 
cout << "Valor de j: "<< j <<`\n`;
```
**Pregunta**
>- ¿Qué hará el siguiente código? 
``` cpp
int x[] = {1, 2, 3};
int *punt = x;
```