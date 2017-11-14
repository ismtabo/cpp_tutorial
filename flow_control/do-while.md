_do while_
====

Este bucle es en esencia idéntico que el anterior, con la única diferencia de que la comprobación de la condición se hace al final; es decir, el contenido dentro del bucle se ejecutará al menos una vez.

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
> - Modifica el código anterior con la función `.sleep_for(chrono::seconds(1) )`[[referencia]](http://www.cplusplus.com/reference/thread/this_thread/sleep_for/) para que el programa espera un segundo por cada iteración, y no se ejecute todo seguido.
> - Cree un código que dado un string por entrada estandar, vaya imprimiendo el string quitando por cada vuelta el último caracter, hasta que quede vacío.