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
    * `while` evalúa la expresión `n>0`
    * Como esta es cierta ejecuta el conjunto de instrucciones agrupadas por `{}`.
    * Imprime por pantalla el valor de n(10) seguido de una coma,
    * y decrementa el valor de n(9).
    * `while` vuelve a evaluar la expresión,
    * y como es verdadera repetirá el conjunto de operaciones.
    * Esto se repetirá hasta que al decrementar `n`, esta sea igual a 0(la condición no se cumpla)
* `while` evalúa la expresión y esta no se cumple.
* Se ignora el conjunto de sentencias y se prosigue con la ejecución.
* Se ejecuta la sentencia `cout<<"Despegue!\n";`

Como vemos el bucle se repite en este caso un número de veces determinado ya que la condición se evalúa sobre un valor numérico, y existe un decremento dentro del conjunto de código. Esta evaluación se puede hacer con cualquier expresión lógica que hemos visto con anterioridad.

**Pregunta**
> - ¿Qué pasaría si la condición siempre se cumpliese?

**Ejercicio**
> - Modifica el código anterior con la función `.sleep_for(chrono::seconds(1) )`[[referencia]](http://www.cplusplus.com/reference/thread/this_thread/sleep_for/) para que el programa espera un segundo por cada iteración, y no se ejecute todo seguido.
> - Cree un código que dado un string por entrada estándar, vaya imprimiendo el string quitando por cada vuelta el último carácter, hasta que quede vacío.


