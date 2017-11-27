# Arrays y Funciones

El nombre del array es un puntero a la posición en memoria del primer elemento.
Si se quiere pasar un array como parámetro de una función hay que hacerlo mediante referencia, es decir, pasar el nombre del array a la función. Existe un problema, y es que la función desconoce el tamaño del array y nos podemos salir.

```cpp
#include <iostream>
using namespace std;

/*Función de inicialización del array*/
icicalizarArray(int * x, int tam);

/*Función para imprimir el array*/
imprimirArray(int * x, int tam);


int main ()
{
 int vector[5];
 icicalizarArray(vector, 5);
 imprimirArray(vector, 5);
 
 return 0;
}

icicalizarArray(int * x, int tam)
{
 int contador=0;
 for(int& n : x)  {
    n=contador;
    contador++;
  }
}


imprimirArray(int * x, int tam)
{
 for(int n : x)  {
    cout<< n<< " ";
  }
  cout << '\n';
}
}


```