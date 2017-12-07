_stringstream_
====

`<sstream>` define un tipo llamado `stringstream` que nos permite tratar un string como un stream, eso nos permite la inserción y la extracción desde y a strings de la misma manera que podríamos hacer con `cin` y `cout`. De forma que podríamos extraer de un string:

```cpp
string mystring ("21");
int age;
stringstream(mystring) >> age;
```

Esto es equivalente a aquello que hicimos en el apartado anterior de `cin`, pero tomando el string `mystring` como _stream_ fuente.

Veamos un ejemplo más completo en el que usaremos la variable `mystring` como buffer de entrada, a la que insertaremos los valores que leamos por teclado y desde la que asignaremos los valores a las variables internas.

```cpp
#include <iostream>
#include <string>
#include <sstream>
using namespace std;

int main ()
{
  string mystring;
  float price=0;
  int quantity=0;

  cout << "Introduce price: ";
  getline (cin,mistring);
  stringstream(mistring) >> precio;
  cout << "Introduce quantity: ";
  getline (cin,mistring);
  stringstream(mistring) >> quantity;
  cout << "Final price: " << price*quantity << endl;
  return 0;
}
```

**Ejercicios**
> - Repita los ejercicios anteriores pero combinando lo que hemos visto de _stringstreams_. Usando un string `stdbuffer` como buffer intermediario entre la entrada y las variables internas.
> - Pruebe a insertar valores en el string utilizado como buffer. _Consejo_: puedes obtener más documentación sobre los _stringstreams_ en la siguiente referencia de [**C++**](www.cplusplus.com/reference/sstream/)
