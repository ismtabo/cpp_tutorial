Definiciones del pre-procesador (_#define_)
====

También puede hacerse uso del pre-procesador para crear variables constantes mediante la sentencia:
`#define identifier replacement`
Esto hace que el **pre-procesador** interprete las coincidencias de `identifier` por `replacement`.

```cpp
#include <iostream>
using namespace std;

#define PI 3.14159
#define NEWLINE '\n'

int main ()
{
  double r=5.0;               // radius
  double circle;

  circle = 2 * PI * r;
  cout << circle;
  cout << NEWLINE;

}
```

Como `#include` las sentencias `#define` son directivas del **pre-procesador** y no necesitan `;`.

**Aviso**: el reemplazado significa que si el define es un cálculo complejo de una variable, este se repetirá todas aquellas veces en las que se encuentre el identificador.

