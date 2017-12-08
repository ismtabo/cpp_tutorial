# Inicialización

Hemos visto que para inicializar una variable se hace uso de la declaración:

```cpp
int x = 0;
```

Pero existen más opciones. Como son las sentencias:

```cpp
int x(0); // Don't mixed up with function declaration
int x{0};
```

**Aviso**: _Este último inicializador sólo está disponible a partir del estándar _`C++11`_, esto significa que para compilarlo necesitaremos usar la opción _`-std=c++11`_ con dicho estándar o posteriores._

Código de ejemplo:

```cpp
// Variable initilizations

#include <iostream>
using namespace std;

int main ()
{
  int a=5;               // Initial value: 5
  int b(3);              // Initial value: 3
  int c{2};              // Initial value: 2
  int result;            // Variable without initial value

  a = a + b;
  result = a - c;        // Initialization of variable `result`
  cout << result;

  return 0;
}
```

Salida

```bash
6
```

> * Modifique el ejemplo anterior para que a, b, y c sean variables de punto flotante inicializadas en 5.0, 3.4, 2.11
> * Pruebe si puede utilizarse para inicializar caracteres.
