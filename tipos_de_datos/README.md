Tipos de datos
====

Como en la mayoría de los lenguajes el operador para la declaración de variables es el `=`.

```cpp
a = 5;
b = 2;
a = a-1;
result = a - b;
```

El tipado de **C++** el tipado es **fuerte**, **estático** y **nominativo**. Recordando, esto significa que _no se pueden usar una variable definida con un tipo concreto como si fuera de otro distinto_(_fuerte_), _una vez declarado el tipo de una variable este no puede cambiar_ (_estático_) y _los tipos de las variables son declaradas por el programador_ (_nominativo_).

Tipos fundamentales

| Grupo | Nombre de tipo | Tamaño |
|--------|--------|-------|
| Caracter | `char` | 8bits |
| Entero (_signed_) | `signed (short,long{0,2}) int, char` | 8~64bits |
| Entero (_unsigned_) | `unsigned (short,long{0,2}) int, char` | 8~64bits |
| Punto flotante | `float, double,  long double` | |
| Booleano | `bool` ||
| Tipo vacío | `void` || 
| Puntero nulo | `decltype(nullptr)` ||


Pero veamos que tipos de datos hay en **C++** y como podemos generar los nuestros propios.
