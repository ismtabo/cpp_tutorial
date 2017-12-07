Asignación ternaria
====

Al igual que **C**, **C++** también nos permite asignar un valor u otro según una condición. Esto se hace de mediante la siguiente sentencia:

`condition ? value1 : value2`

Es decir, si `condition` se evalúa `value1` sino `value2`.

Veamos el siguiente ejemplo:

```cpp
#include <iostream>
using namespace std;

int main ()
{
  int a,b,c;

  a=2;
  b=7;
  c = (a>b) ? a : b;

  cout << c << '\n';
}
```

**Pregunta**
> ¿Qué función se estaría resolviendo con el código anterior?