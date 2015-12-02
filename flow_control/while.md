_while_
====

El bucle `while` posiblemente sea el más sencillo de entender de todos, su estructura es la siguiente:

while (condicion) sentencia

Este bucle primero mira la `condicion` y si esta se cumple permite ejecutar la `sentencia`, acto seguido volverá a evaluar la `condicion`, y si esta vuelve a ser verdadero, repetirá la ejecución de la `sentencia`. Esto permite que seguir repitiendo la `sentencia` siempre que se cumpla la `condición`. Veamos el siguiente caso de ejemplo:

```cpp
#include <iostream>
using namespace std;

int main ()
{
  int n = 10;

  while (n>0) {
    cout << n << ", ";
    --n;
  }

  cout << "¡Despegue!\n";
}
```

El flujo del anterior código de la siguiente manera:
* Se asigna a `n` el valor 10.
* Comienza la ejecución del bucle:  
    * `while` evalua la expresión `n>0`
    * Como esta es cierta ejecuta el conjunto de instrucciones agrupadas por `{}`.
    * Imprime por pantalla el valor de n(10) seguido de una coma,
    * y decrementa el valor de n(9).
    * `while` vuelve a evaluar la expresión,
    * y como es verdadera repetirá el conjunto de operaciones.
    * Esto se repetirá hasta que al decrementar `n`, esta sea igual a 0(la condición no se cumpla)
* `while` evalua la expresión y esta no se cumple.
* Se ignora el conjunto de operacionessentencias y se prosigue con l a ejecución.
* Se ejecuta la sentencia `cout<<"Despegue!\n";`

Como vemos el bucle se