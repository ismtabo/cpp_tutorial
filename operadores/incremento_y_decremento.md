Incremento y decremento
====

Las asignaciones compuestas para las operaciones de suma y resta tienen otra variante más acortada, donde la parte derecha de la operación toma el valor unitario (`1`). Estás alternativas son respectivamente, `++` y `--`.

```cpp
#include <iostream>
using namespace std;

int main ()
{
  int a, b=3;
  a = b;
  b = a++;
  a = ++b;
  cout << a <<endl;
  cout << b;
}
```
> - ¿Cuál será el resultado del código anterior? ¿En qué se diferencia `a++` de `++b`?
> - ¿Te esperabas el resultado?

Las operaciones de incremento `++` y decremento `--` nos dan a entender que son equivalentes a las sentencias vistas en el apartado anterior:
```cpp
a += 1
a -= 1
```

Pero hay una diferencia según la precedencia del operador. Según ejecutemos `x++` o `++x` el resultado será distinto, de manera igual para el decremento.

Veamos los siguientes ejemplos:

**++x**
```cpp
x = 3;
y = ++x;
//x contiene 4, y contiene 4
```

**x++**
```cpp
x = 3;
y = x++
// x contiene 4, y contiene 3
```

Esta diferencia se produce ya que cuando operamos con `x++` la primera operación que se ejecuta es la asignación, y después se incrementa:
```cpp
y = x;
x += 1;
```

En cambio, con `++x`, ocurre al revés:
```cpp
x += 1;
y = x;
```

Ocurriendo lo mismo con el decremento.

**Aviso**: esta diferencia puede ser importante según su uso en los programas, ya que hay que tener en cuenta el orden de la asignación y el in/decremento cuando estemos asignando o comparando con otra variable, o al ser parte de una operación mayor.