# Array/Vectores

Un array es una asignación contigua de memoria donde se almacena una colección de datos todos del mismo tipo. Hay varios tipos de vectores multidimensionales y unidimensionles.
La declaración de los arrays en c/c++ son las siguiente:
```
tipo nombre[tamaño];
tipo nombre[]={valor1, valor2, ...}
```
Para acceder a sus valores es la siguiente:
```
nombre [i]
```
*i*  es una variables de tipo `int` y representan la posición del elemento dentro del array. Se empieza a contar siempre por el 0 para acceder al primer elemento del array.

Un ejemplo:

```cpp
#include <iostream>
using namespace std;

int main ()
{
 int vector[5];
  for(int n=0; n<5; n++)  {
     vector[n]=n+1;
  }
  for(int n=4; n>=0; n--)  {
     cout<<vector[n];
  }

}
```
**Pregunta**
>- ¿Cual es la diferencia entre `vector[i][j]` y `vector[i]`?, ¿Cual es la salida del código anterior?

**Ejercicio**
>- Modificar el código anterior para que los elementos del vector vayan de mayor a menor y se impriman de menor a mayor.
