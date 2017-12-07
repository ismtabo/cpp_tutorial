## Operaciones con clase _string_

Como pensarás la clase string tiene más operaciones que la asignación, veamos una pequeña introducción a las capacidades de esta clase.

```cpp
#include <iostream>
#include <string>
using namespace std;

int main ()
{
  string name ("John");
  string family ("Smith");
  name += " K. ";         // c-string
  name += family;         // string
  name += '\n';           // character

  cout << name;
  return 0;
}
```

> ¿Cuál será la salida del programa anterior?

El operador `+=` sobre un string añadira el c-string, string o carácter que indiquemos al final del string. También se puede añadir mediante el operador `.append( . )`.

> Modifique el código de ejemplo anterior reemplazando el operador `+=` con el operador de clase `.append( . )`

Más operadores de la clase `string`:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main ()
{
  string name ("John");

  cout<<name.at(0)<<endl;
  cout<<name.size()<<endl;
  return 0;
}
```

> ¿Qué salida esperamos en el código anterior?

Operadores de acceso a un elemento: `.at()`, `[]`, `.back()`, `.front()`.  
Operadores para conocer el tamaño del string: `.size()`, `.length()`

Más información: [referencia](http://www.cplusplus.com/reference/string/string/)

