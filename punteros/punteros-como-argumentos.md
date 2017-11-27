# Punteros como argumentos de funciones

Vimos al hablar de funciones que los parámetros se podían pasar por valor o por referencia\* usando punteros. En este segundo caso, pasamos a la función la dirección de la variable, por lo que si modificamos el contenido de esa dirección, esa modificación será vista al acabar la ejecución de la función. Ésta es una manera de que una función pueda modificar variables de la función que la llamó.
Ejemplo:

```cpp
 #include <iostream>
/* Prototipo */
void cambia (int *var1, int *var2);
int main ()
{
  int i=1, j=2;
  printf ("Valores antes de funcion Cambia: i=%d, j=%d", i, j);
  Cambia (&i, &j);
  printf ("Valores despues de funcion Cambia: i=%d, j=%d", i, j);
  }
/* Definición */
void cambia (int *a, int *b)
  {
  int tmp;
  tmp = *a;
  *a = *b;
  *b = tmp;
  }
```
\*pasar por referencia se pasa la dirección de memoria de la variable y no su valor.







