_if-else_
====

_if-else_ es una sentencia de control que nos permite tomar decisiones sobre el flujo del programa. Según una condición decidiremos si ejecutamos o no una/s sentencia/s de código de la forma:

`if (condicion) sentencia`

Esta `condicion` es evaluada, si se cumple la `sentencia` será ejecutada. En caso contrario la `sentencia` sera ignorada, siguiendo con la ejecución del programa. Como se produce en el siguiente ejemplo.

```cpp
if (x==100)
    cout << "x es 100";
```

Este código imprimirá "x es 100", si la condición es cierta, y sino no se imprimirá nada.

También se puede agrupar un conjunto de sentencias mediante llaves:

```cpp
if (x == 100)
{
   cout << "x es ";
   cout << x;
}
```

Normalmente se usa la identación para mostrar un código más legible, pero podemos expresar el código anterior de la siguiente manera también:

```cpp
if (x == 100) { cout << "x is "; cout << x; }
```

De la misma manera podemos decidir sobre dos conjuntos de sentencias, para elegir cual ejecutar.

`if (condicion) sentencia1 else sentencia2`

Donde la `sentencia1` será ejecutada si la `condicion` es verdadera sino se ejecutará la `sentencia2`. Por ejemplo:

```cpp
if (x == 100)
  cout << "x es 100";
else
  cout << "x no es 100";
```

Por última variedad, podemos anidar condiciones como en el ejemplo siguiente:

```cpp
if (x > 0)
  cout << "x es positivo";
else if (x < 0)
  cout << "x es negativo";
else
  cout << "x es 0";
```

En este caso, decidimos sobre tres sentencias que se irán resolviendo según se vayan considerando las condiciones en orden de ejecución, sabiendo que si no se cumple una condición encapsulada en un `if` se sigue en el `else` correspondiente.

**Ejercicio**
> - Recogiendo por entrada estandar dos palabras separadas por un espacio en blanco. Imprima cuál de las dos es tiene mayor longitud, imprimiendo la palabra seguida por la longitud.
> - Haciendo uso de `if-else` calcule el valor absoluto de un número introducido por entrada estandar. _Consejo_: Por si no te acuerdas de cómo se calculaba el valor absoluto, te damos un empujón. [Wikipedia - Valor absoluto](https://es.wikipedia.org/wiki/Valor_absoluto)