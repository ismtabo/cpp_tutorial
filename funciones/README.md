# Funciones
En el lenguaje C/C++ una función se define de la siguiente manera:
```cpp
type name(type_param1 param1, type_param param2 [, ...])
{
    /* Function body */
    ...
    [return value;]
}
```
Donde:
- **type** es el tipo del dato que devuelve. Si no devuelve nada se declara de tipo ```void```. Si no se especifica tipo se asume que es entero.
- **name** es el nombre con el que se identifica la función.
- **Parámetros de la función** `(type_param1 param1, type_param param2 [, ...])`:<br> es una lista de nombres de variables separados por comas con sus tipos asociados., que recibirán valor en el momento de llamar a la función. Los paréntesis siempre deben aparecer, aunque la función no tenga argumentos. Estas variables sólo estarán definidas dentro de la función, es decir, son locales a la función, salvo que hayan sido definidas como globales, creándose al comienzo de la ejecución de la función y destruyéndose al finalizar ésta. Esto es aplicable a cualquier otra variable declarada dentro de la función.
- La sentencia **return** es opcional, sólo debe aparecer si la función retorna un valor. Puede aparecer en cualquier punto del cuerpo de una función.
