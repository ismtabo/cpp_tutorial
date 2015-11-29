Operadores
====

Operador de asignación(=)
----

```cpp
#include <iostream>
using namespace std;

int main ()
{
  int a, b;
  a = 10;
  b = 4;
  a = b;
  b = 7;

  cout << "a:";
  cout << a;
  cout << " b:";
  cout << b;
}
```

> ¿Cuál será la salida del código anterior?

Como hemos visto en el punto anterior de los _Tipos_ este tipo nos sirve para dar valor a una variable, veamos otros usos de este operador:

```cpp
y = 2 + (x = 5);
```

> ¿Es esta asignación correcta? ¿O dará error de compilación/ejecución?

La anterior sentencia asignará a `y` el resultado de sumar a 2 el valor resultante de la asignación, es decir, equivale a las siguientes sentencias:
```cpp
x = 5;
y = 2 + x;
```
Agrupación de asignaciones:
```cpp
#include <iostream>
using namespace std;

int main ()
{
  int x, y ,z;
  x = y = z = 5;

  cout << "x:";
  cout << x;
  cout << " y:";
  cout << y;
  cout << " z:";
  cout << z;
}
```
> ¿Cuál es la salida del código anterior?

Como observamos, también podemos agrupar asignaciones del mismo valor a un conjunto de variables.



