# for-in

Este bucle sirve para recorrer sobre colecciones de datos y estructuras iterables (_array_ / `vector`) y acceder a sus valores directamente. Veamos la estructura general del bucle:
```
for(type_iterator iterator: iterable)
  statement
```

Veamos un ejemplo de iteración sobre un _array_ de enteros, el funcionamiento del cuál se verá más adelante.

```cpp
#include <iostream>
using namespace std;

int main ()
{
  int numbers[]={1,2,3,4,5,6,7};
  for(int n : numbers)  {
    cout << n << ", ";
  }

  cout << "Blast-off!\n";
  
  return 0;
}
```

Su salida sería:
```
1, 2, 3, 4, 5, 6, 7, Blast-off!
```

Esto nos permite recorrer la lista `numbers`, pero no nos permite modificar el valor que contiene el iterador `n`. Para poder modificar el valor podríamos utilizar `n` como referencia con `&n` (el uso de referencia se explicará más adelante):

```cpp
int main ()
{
  int numbers[]={1,2,3,4,5,6,7};
  for(int& n : numbers)  {
    cout << n << ", ";
    n++;
  }

  cout << "Blast-off!\n" << endl;
  
  for(int n: numbers) {
    cout << n << ", ";
  }
  
  return 0;
}
```

Su salida sería:
```
1, 2, 3, 4, 5, 6, 7, Blast-off!
2, 3, 4, 5, 6, 7, 8, 
```

Como vemos, los valores de la lista se han modificado.

Es **importante** remarcar que esto solo funciona con el **estándar 11 de C++**