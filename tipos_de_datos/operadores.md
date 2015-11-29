Operadores
----

###Operador de asignación(=)
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

###Operadores aritméticos, bit a bit, evaluación y lógicos
| Aritméticos | Uso || _bitwise_ | Uso |
|:--------:|--------||:-------:|-----|
| + | Suma || & | AND |
| - | Resta || &#124; | OR | 
| * | Multiplicación || ^ | XOR |
| / | División || ~ | NOT |
| % | Módulo || << | Desplazamiento a la izquierda |
||||>>| Desplazamiento a la derecha | 

| Comparación | Uso || Lógico |Uso|
|:----:|------||:----:|-----|
| == | Igual || ! | Negación |
| != | Diferente || && | AND lógico |
| < | Menor que || &#124;&#124; | OR lógico
| > | Mayor que |
| <= | Menor o igual que |
| >= | Mayor o igual que ||

###Asignación compuesta <small><small>(+=, -=, *=, /=, %=, >>=, <<=, &=, ^=, |=)</small></small>
```cpp
#include <iostream>
using namespace std;

int main ()
{
  int a, b=3;
  a = b;
  a+=2;
  cout << a;
}
```
> ¿Qué valor tendrá `a` al final de la ejecución?

Es decir, `a+=2` es equivalente a:
```cpp
a = a + 2;
```

###Incremento y decremento <small><small>(++,&#45;&#45;)</small></small>

