_do while_
====

Este bucle es en esencia idéntico que el anterior, con la única diferencia de que la comprobación de la condición se hace al final; es decir, el contenido dentro del bucle se ejecutará al menos una vez. La estructura general de este bucle es el siguiente:

`do statement while(condition);`

Veamos un ejemplo:

```cpp
#include <iostream>
using namespace std;

int main ()
{
  int n = 10;

   do{
    cout << n << ", ";
    --n;
  }while (n>0)

  cout << "¡Despegue!\n";
}
```


**Pregunta**
> - ¿Qué pasaría si la condición siempre se cumpliese?

**Pregunta 2**
> - ¿Qué pasaría si n=-1  antes de empezar el bucle y la condición sea n>1?





**Ejercicio**
> - Cree un código que dado un string por entrada estandar, vaya imprimiendo el string quitando por cada vuelta el último caracter, hasta que quede vacío.
