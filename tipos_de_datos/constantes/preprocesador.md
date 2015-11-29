Definiciones del preprocesador (_#define_)
====

También puede hacerse uso del preprocesador para crear variables constantes mediante la sentencia:
`#define identifier replacement`
Esto hace que el **preprocesador** interprete las coincidencias de `identifier` por `replacement`.

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

Como `#include` las sentencias `#define` son directivas del **preprocesador** y no necesitan `;`.
