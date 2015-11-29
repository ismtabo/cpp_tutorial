Expresiones tipadas constantes
====

A veces es conveniente dar un nombre a un valor constante:

```cpp
#include <iostream>
using namespace std;

// Expresiones constantes
const double pi = 3.14159;
const char newline = '\n';

int main ()
{
  double r=5.0;               // radius
  double circle;

  circle = 2 * pi * r;
  cout << circle;
  cout << newline;
}
```

De esta manera no tendremos que podremos reutilizar el literal todas las veces que queramos, y en caso de necesitar cambiarlo sólo habría que modificar el valor inicialmente asignado.

> Intente modificar el literal constante `pi` y fíjese en el error producido.