Entrada estandar (_cin_)
====

Como en la mayoría de entornos de programación, la entrada estandar es por teclado, y en **C++** está definido el objeto _stream_ `cin`.

Para entradas formateadas se hace uso de `cin` con el operador de extracción `>>`. Como por ejemplo:

```cpp
int edad;
cin >> edad;
```

En el caso de ejemplo, en la primera sentencia declaramos la variable entera `edad`, y la segunda extrae un valor de `cin` y la asigna a la variable. La entrada mediante `cin` se introduce cuando se pulsa la tecla `ENTER` o `RETURN`. Esto implica que la ejecución del programa no sigue hasta que se haya completado la lectura por teclado, es decir la sentencia `cin` se complete. 

La extracción del _stream_ mediante `cin` usa el tipo de la variable a la que se le asigna el valor externo determinando como debe interpretar la entrada; en caso de ser un entero, se esperará una serie de dígitos como formato de entrada, si es string se espera una secuencia de caracteres, etc.

```cpp
#include <iostream>
using namespace std;

int main ()
{
  int i;
  cout << "Please enter an integer value: ";
  cin >> i;
  cout << "The value you entered is " << i;
  cout << " and its double is " << i*2 << ".\n";
  return 0;
}
```

Como vemos la entrada mediante `cin` es bastante sencilla y clara, gracias a la abstracción del _stream_ que se encarga del formato y la conversión de la entrada al tipo correspondiente.

Al igual que con la inserción ce puede extraer `cin` en varias variables en la misma sentencia, como en el siguiente ejemplo:

```cpp
cin >> a >> b;
```
Sería equivalente a:

```cpp
cin >> a;
cin >> b;
```

