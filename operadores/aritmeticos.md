Operadores aritméticos, bit a bit, evaluación y lógicos
====

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

Asignación compuesta <small><small>(+=, -=, *=, /=, %=, >>=, <<=, &=, ^=, |=)</small></small>
----

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

Incremento y decremento <small><small>(++,&#45;&#45;)</small></small>
----