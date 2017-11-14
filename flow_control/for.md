# for
Este bucle a diferencia de los dos anteriores, se usa para iterar sabiendo el número de veces que se va a hacer. Su estructura es la siguiente:
``` 
for(inic; exp_booleana ; actuaizar)
    sentencia
```
Esto en un código C++ se traduce en:
```cpp
#include <iostream>
using namespace std;

int main ()
{
  for(int n=0; n<=10; n++)  {
    cout << n << ", ";
  }

  cout << "¡Despegue!\n";
}
```
El flujo del código anterior es el siguiente:
- Se asigna a n el valor 0
- Comprueba que n es menor que 10
- Comienza la ejecución del bucle
  - Imprime por pantalla el valor de n(0)
  - se incrementa el valor n(1).
  - `for`evalúa la expresión,
  - como es verdadera repetirá las operaciones.
  - Esto se repetirá hasta que n sea igual a 10 (que la condición se cumpla

