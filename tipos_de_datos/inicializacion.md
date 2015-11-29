Inicialización
====

Hemos visto que para inicializar una variable se hace uso de la declaración:
```cpp
int x = 0;
```

Pero existen más opciones. Como son las sentencias:
```cpp
int x(0);// no confundir con la declaración de funciones 
int x{0};
```
**Aviso**: _Este último inicializador sólo está disponible con el estandar `C++11`, esto significa que para compilarlo necesitaremos usar la opción `-std=c++11`._

Código de ejemplo:
```cpp
// inicialización de variables

#include <iostream>
using namespace std;

int main ()
{
  int a=5;               // valor inicial: 5
  int b(3);              // valor inicial: 3
  int c{2};              // valor inicial: 2
  int result;            // valor inicial sin determinar

  a = a + b;
  result = a - c;
  cout << result;

  return 0;
}
```
Salida
```bash
6
```

>- Modifique el ejemplo anterior para que a, b, y c sean variables de punto flotante inicializadas en 5.0, 3.4, 2.11
>- Pruebe si puede utilizarse para inicializar caracteres.
