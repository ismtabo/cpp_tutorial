Salida estandar (_cout_)
====

Conocidos los tipos de _stream_ conozcamos como interactuar con ellos.

La salida estandar de **C++** por defecto es la impresión por pantalla, y la instancia indicada para esta operación es `cout`. Para la salida del programa usaremos el operador de inserción `<<`.

```cpp
cout << "Salida del programa"; // imprime Salida del programa por pantalla
cout << 120;               // imprime number 120 por pantalla
cout << x;                 // imprime el valor de x por pantalla
```

La salida del anterior código será según vayamos insertando en la instancia de `cout`.

El operador `<<` distinguirá entre literales y variables, pero no entre tipos de datos básicos que vimos en el primer apartado, es decir, que podremos insertar elementos de distintos tipos sin tener que _castear_ las variables.

```cpp
cout << "Hola";  // imprime Hola
cout << Hola;    // imprime el contenido de la variable Hola
```

Se puede usar este operador para insertar varios elementos en la misma línea con una sentencia.

```cpp
cout << "Este " << " es una " << "única sentencia de C++";
```

Esta sentencia es útil al querer mezclar literales y variables para formatear la salida, como hacemos en el siguiente ejemplo.

```cpp
cout << "Tengo " << age << " años y mi codigo postal es " << codigo_postal;
```

Suponiendo que la variable `age` contiene el valor 24 y el `codigo_postal` contiene el valor 47001. La salida será 

`Tengo 24 años y mi codigo postal es 47001`

Pero como ocurría con _printf_ en **C**, `cout` no imprime un salto de línea al final de la impresión. Podemos solucionar esto mediante la inserción de código de escape de nueva línea al `\n` o mediante `endl`(`std::endl`), que inserta exactamente ese carácter en el _stream_ de salida. Ejemplo:

```cpp
cout << "Primera sentencia." << endl;
cout << "Segunda sentencia." << endl;
```
Salida
```bash
Primera sentencia.
Segunda sentencia.
```

**Ejercicios**
> - Imprime por pantalla tu nombre y tu edad separados por un espacio.
> - Imprime por pantalla, dadas dos variables enteras `a = 2` y `b = 3`, la suma de estas dos variables formateda de la siguiente manera:<br>`La suma de <a> y <b> es <suma>`
> - Imprime un texto cualquiera con más de una línea mediante dos sentencias distintas y mediante una sentencia. _Consejo_: `endl` no sólo puede usarse para insertarse al final de la sentencia, sino también en medio de ella.




