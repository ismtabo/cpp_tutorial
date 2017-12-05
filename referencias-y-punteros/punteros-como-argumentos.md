# Punteros como argumentos de funciones

Hemos hablado de parámetros que pueden pasarse por valor o por referencia. En este segundo caso, ya vimos como podía pasarse mediante el uso de **referencias** con el operador `&`. En este caso vamos a aclarar como se pueden pasar por referencia mediante el uso de **punteros**. 

Al utilizar un puntero como parámetro de una función, pasamos la **dirección de la variable**, por lo que si modificamos el contenido de esa dirección, esta se va a ver alterada al acabar la ejecución de la función. 

Ejemplo:

```cpp
#include <iostream>
using namespace std; 
 
/* Prototype */
void swap (int*, int*);

/* Main */
int main ()
{
  int i=1, j=2;
  cout << "Values of i and j before swap: ";
  cout << i << " " << j << endl;
  
  swap(&i, &j);
  cout << "Values of i and j after swap: ";
  cout << i << " " << j << endl;
}
  
/* Definition */
void swap (int *a, int *b)
  {
  int tmp;
  tmp = *a;
  *a = *b;
  *b = tmp;
  }
```
\*pasar por referencia se pasa la dirección de memoria de la variable y no su valor.







