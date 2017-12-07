# Arrays y Funciones

El nombre del array es un puntero a la posición en memoria del primer elemento.  
Si se quiere pasar un array como parámetro de una función hay que hacerlo mediante referencia, es decir, pasar el nombre del array a la función. Existe un problema, y es que la función desconoce el tamaño del array y nos podemos salir.

Existen varias formas de representar este puntero en la cabecera de la función:

* Estas dos formas funcionan exactamente igual, aun que conceptualmente representan lo mismo.

```cpp
void method(int *array);
```

o

```cpp
void method(int array[]);
```

* Esta forma de pasar el array le indicas cual es el tamaño que tendrá y si no coincide dará error.

```cpp
void method(int array[size_of_the_array]);
```

Como dentro de la función no se conoce el tamaño del array, es común añadir un parámetro que acompañe a cada array con el tamaño de este, de manera que la definición de parámetros sea la siguiente:  

```cpp
void method(int array[], int array_size)
```

Esta estructura se ameja a la definición de parámetros de la función `main`:
```cpp
int main(int argc, char** argv)
```

La cual tiene como parámetros, el número de argumentos que se le pasa `argc` y el vector de cadenas de caracteres que contiene `argv`.


Ejemplo de código:

```cpp
#include <iostream>
using namespace std;

/*Function which initialize array*/
void initializeArray(int x[], int tam);

/*Function which prints array at stdout*/
void printArray(int x[], int tam);


int main ()
{
 int array[5];
 initializeArray(array, 5);
 printArray(array, 5);

 return 0;
}

void initializeArray(int x[], int tam)
{
 int contador=0;
 for(int i=0; i< tam; i++)  {
    x[i]=i;
  }
}


void printArray(int x[], int tam)
{
 for(int i=0; i< tam; i++)  {
    cout<< x[i]<< " ";
  }
  cout << '\n';
}
```



