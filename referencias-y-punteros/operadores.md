# Operadores
Existen dos operadores especiales relacionados con punteros:
- El operador "**&**"(dirección de): devuelve la dirección de memoria donde está asignada una determinada variable:.
```c
int *i,j;
j=5;
i=&j;  // Asign memory address of j to i
```
- El operador "__*__"(valor de): asociado a un puntero devuelve el valor del contenido en la dirección de memoria a la que apunta el puntero.
```cpp
cout << "Hexadecimal memory addres of j: 0x"<< hex<< i <<`\n`;
// Retrieve value from pointer
cout << "Valor de j: "<< *i <<`\n`;
// Get value from variable
cout << "Valor de j: "<< j <<`\n`;
```
**Pregunta**
>- ¿Qué hará el siguiente código? 
``` cpp
int x[] = {1, 2, 3};
int *punt = x;
```