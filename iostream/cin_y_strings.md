_cin_ y _strings_
====

La extracción de `cin` a _string_ se hace de la misma manera que para otros tipos de datos:

```cpp
string mystring;
cin >> mystring;
```

En cambio, `cin` considera también los caracteres de espacio como un carácter de finalización de un string, esto puede suponer un problema al extraer palabras, frases o sentencias completas. Eso puede solucionarse mediante el uso de la función `getline` que opera con un _stream_ (`cin`) como primer argumento y un _string_ como segundo. Por ejemplo:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main ()
{
  string mystr;
  cout << "What's your name? ";
  getline (cin, mystr);
  cout << "Hello " << mystr << ".\n";
  cout << "What is your favorite team? ";
  getline (cin, mystr);
  cout << "I like " << mystr << " too!\n";
  return 0;
}
```

De esta manera, se obtendrá el contenido de la línea entera, esperando la pulsación de la tecla ENTER (o RETURN) para finalizar la extracción.

**Ejercicio**
> Lea por teclado dos líneas, una primera que contenga su nombre y primer apellido, y una segunda línea que tome el día y el mes de nacimiento separados por un espacio. El programa deberá imprimir por pantalla tus iniciales junto con la fecha de nacimiento con el formato `dd/mm`.
