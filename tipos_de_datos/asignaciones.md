Asignaciones
====

Declaración y operaciones sobre variables
```cpp
#include <iostream>
using namespace std;

int main ()
{
  // declaración de variables:
  int a, b;
  int result;

  // operaciones:
  a = 5;
  b = 2;
  a = a + 1;
  result = a - b;

  // impriendo el resultado:
  cout << result;

  // finalización del problema:
  return 0;
}
```
Salida
```bash
4
```

En el caso anterior hemos dado un ejemplo en el que operamos con las distintas variables declaradas. Como has podido observar hemos operado sobre enteros y luego hemos imprimido por pantalla el resultado.

>- ¿Cómo harías para operar sobre tipos de coma flotante?
>- ¿Es posible sumar un entero a un float, o a un caracter?¿Cuál es el resultado final?