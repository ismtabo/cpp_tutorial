Salida estandar (_cout_)
====

Conocidos los tipos de _stream_ conozcamos como interactuar con ellos.

La salida estandar de **C++** por defecto es la impresión por pantalla, y la instancia indicada para esta operación es `cout`. Para la salida del programa usaremos el operador de inserción `<<`.

```cpp
cout << "Output";          // Print `Output` by standard output
cout << 120;               // Print number 120 by standard output
cout << x;                 // Print value of x by standard output
```

La salida del anterior código será según vayamos insertando en la instancia de `cout`.

El operador `<<` distinguirá entre literales y variables, pero no entre tipos de datos básicos que vimos en el primer apartado, es decir, que podremos insertar elementos de distintos tipos sin tener que _castear_ las variables.

```cpp
cout << "Hola";  // imprime Hola
cout << Hola;    // imprime el contenido de la variable Hola
```

Se puede usar este operador para insertar varios elementos en la misma línea con una sentencia.

```cpp
cout << "This " << " is a " << "single statement of C++";
```

Esta sentencia es útil al querer mezclar literales y variables para formatear la salida, como hacemos en el siguiente ejemplo.

```cpp
cout << "I am " << age << " years old and my postal code is " << postal_code;
```

Suponiendo que la variable `age` contiene el valor 24 y el `postal_code` contiene el valor 47001. La salida será 

`I am 24 years old and my postal code is 47001`

Pero como ocurría con _printf_ en **C**, `cout` no imprime un salto de línea al final de la impresión. Podemos solucionar esto mediante la inserción de código de escape de nueva línea al `\n` o mediante `endl`(`std::endl`), que inserta exactamente ese carácter en el _stream_ de salida. Ejemplo:

```cpp
cout << "First statement." << endl;
cout << "Second statement." << endl;
```
Salida
```bash
First statement.
Second statement.
```

**Ejercicios**
> - Imprime por pantalla tu nombre y tu edad separados por un espacio.
> - Imprime por pantalla, dadas dos variables enteras `a = 2` y `b = 3`, la suma de estas dos variables formateda de la siguiente manera:<br>`Sum of <a> plus <b> is equal to <suma>`
> - Imprime un texto cualquiera con más de una línea mediante dos sentencias distintas y mediante una sentencia. _Consejo_: `endl` no sólo puede usarse para insertarse al final de la sentencia, sino también en medio de ella.




