Introducción a C++
====

Introducción
----

**C++** es un lenguaje de programación diseñado a mediados de los años 80 por *Bjarne Stroustrup*. La intención de su creación fue el extender al lenguaje de programación **C** mecanismos que permiten la manipulación de **objetos**. En ese sentido, desde el punto de vista de los **lenguajes orientados a objetos**, **C++** es un lenguaje híbridos.

Este tutorial está dirigido a aquellas personas que nunca han programado en **C++** y estén a punto de estrenar sus habilidades programadoras en este amplio lenguaje.

**C++** está considerado un lenguaje multiparadigma, entre las que se encuentra la _orientación a objetos_, _imperativo_, o la _programación genérica_. En esta introducción al lenguaje aprenderemos a definir variables, y crear nuestros propios tipos de datos y operadores, manejar las estructuras de control, y la entrada y salida del programa, y a dominar las bases de la creación e implementación de clases y clases genéricas.

Al final de esta **Hour of Code**, espero que **C++** os haya convencido y sea de vuestro gusto para vuestros próximos proyectos, prácticas o para rellenar las aptitudes de **LinkedIn**.
<center>
_Sin más dilación comenzamos con el tutorial._
</center>

###Descripción del tutorial

Para realizar este tutorial se ha dividido en diversas partes según el contenido que se de como, **tipos de datos**, **sentencias de control**... Por cada uno de estos títulos encontrarás una pequeña descripción inicial, y distintos códigos de ejemplo.

También se le propondrán ejercicios que aparecerán como texto resaltado, como en el siguiente ejemplo:
>- ¿Cómo harías para operar sobre tipos de coma flotante?
>- ¿Es posible sumar un entero a un float, o a un caracter?¿Cuál es el resultado final?




Operadores
----
<small><small>[(Arriba)](#)</small></small>
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


