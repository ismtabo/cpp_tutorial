Deducción de tipo
====

Como punto final para explicar los tipos fundamentales, ahora vamos a ver como un tipo puede deducir el tipo de la variable que se le asigna. Estas son las declaraciones `auto` y `decltype(foo)`.

Ejemplos de uso:
```cpp
int a = 0;
auto foo = a;  // mismo resultado que: int bar = foo;
decltype(a) bar;  // mismo resultado que: int bar; 
```
