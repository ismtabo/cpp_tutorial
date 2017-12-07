# Punteros como argumentos de funciones

Hemos hablado de parámetros que pueden pasarse por valor o por referencia. En este segundo caso, ya vimos como podía pasarse mediante el uso de **referencias** con el operador `&`. En este caso vamos a aclarar como se pueden pasar por referencia mediante el uso de **punteros**. 

Al utilizar un puntero como parámetro de una función, pasamos la **dirección de la variable**, por lo que si modificamos el contenido de esa dirección, esta se va a ver alterada al acabar la ejecución de la función. 

Ejemplo con la función de intercambio, que hemos visto en la sección sobre **referencias**:

```cpp
#include <iostream>
using namespace std; 
 
/* Prototype */
void swap (int*, int*);

/* Main */
int main ()
{
  int i=0, j=1;
  cout << "Values of i and j before swap: ";
  cout << i << " " << j << endl;
  
  swap(&i, &j);
  cout << "Values of i and j after swap: ";
  cout << i << " " << j << endl;
}
  
/* Definition */
void swap (int *a, int *b) {
  int tmp;
  tmp = *a;
  *a = *b;
  *b = tmp;
}
```

Al igual que en el caso en el uso de **referencias**, la salida del código anterior será:
```
Values of i and j before swap: 0 1
Values of i and j before swap: 1 0
```
