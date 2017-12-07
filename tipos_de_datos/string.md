# _Strings_

Los string representan un conjunto ordenado de caracteres, literalmente, _una cadena_. En **C++** nos encontramos con la clase _string_ la cual nos permite guardar esa secuencia de caracteres.

La primera diferencia con los tipos que hemos ido viendo hasta ahora, es que esta clase necesita importar su código desde su propia biblioteca estandar `<string>`, por lo tanto deberemos incluirla en la cabecera de nuestro programa. A diferencia de **C**, a los strings no se les trata como un array de caracteres terminado por `\0`, por lo tanto cuando los declaremos no será necesario declararlo como `char cadena[]`, ni reservar un espacio de más para nuestro carácter de finalización.

```cpp
#include <iostream>
#include <string>
using namespace std;

int main ()
{
  string mystring;
  mystring = "This is a string";
  cout << mystring;
  return 0;
}
```

Salida

```bash
This is a string
```

Como hemos visto en el ejemplo anterior, los string se declaran y se le asignan valores de igual forma que los anteriores tipos.

> * Pruebe a asignar nuestra variable `mystring` el valor `This is a string`, e imprimirlo por pantalla.
> * Inicialice dos nuevos string `cadena` y `caracteres`, mediante los operadores de inicialización `( . )` y `{ . }` que hemos visto con anterioridad.



