# for-each
Este bucle sirve para iterar sobre elementos iterables (array) y acceder a sus valores directamente:
```cpp
#include <iostream>
using namespace std;

int main ()
{
  int vector[]={1,2,3,4,5,6,7};
  for(int n : vector)  {
    cout << n << ", ";
  }

  cout << "¡Despegue!\n";
}
```
Esto nos permite recorrer el vector, pero no nos permite modificar el valor que contiene n, otra opción es:

```cpp
int main ()
{
  int vector[]={1,2,3,4,5,6,7};
  for(int& n : vector)  {
    cout << n << ", ";
    n++;
  }

  cout << "¡Despegue!\n";
}
```
Es **importante** remarcar que esto solo funciona con el **estándar 11 de C++**