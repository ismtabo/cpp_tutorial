# Asignación compuesta 

La asignación compuesta trata de una operación especial, donde la variable a la que se va a asignar posteriormente, se incluye como la parte izquierda de la operación. Entre las asignaciones compuestas se incluyen: `+=, -=, *=, /=, %=, >>=, <<=, &=, ^=, |=`.


```cpp
#include <iostream>
using namespace std;

int main ()
{
  int a, b=3;
  a = b;
  a+=2;
  cout << a;
}
```
> ¿Qué valor tendrá `a` al final de la ejecución?

Es decir, `a+=2` es equivalente a:
```cpp
a = a + 2;
```
