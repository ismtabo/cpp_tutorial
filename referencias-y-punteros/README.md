# Referencias y punteros

Existen dos maneras en **C++** para modificar una variable de forma indirecta a través de _enlaces_ a su dirección de memoria. Los **punteros** es una tecnología muy útil, pero a la vez compleja, que se hereda de **C**, que explicaremos más adelante. **C++** introduce una alternativa más simple a los punteros, las __referencias__.

## Referencias

Como hemos dicho, las __referencias__ se consideran una alternativa simple de los punteros, considerando a estos sus hermanos mayores. Una refencia permite tener más de vía de escritura y lectura de una variable. ¿Cómo puede ser esto? Veamos el siguiente ejemplo, sobre el uso común de una referencia sobre una variable tipo entero:

```cpp
int j = 8;
int &i = j;
```

**Aviso**: a diferencia de los punteros (como veremos más adelante), las referencias siempre tienen que ser inicializadas al ser definidas, por lo que un código como el siguiente daría error:
```cpp
int &i;
```
Una vez inicializada, una referencia no se puede cambiar la variable a la que haga referencia. Ya que el operador de asignación cambiará la variable original.

En el caso anterior hemos definido dos variables `j` e `i`. La primera es una variable de tipo primitivo, pero con la segunda hemos utilizado el operador para definir referencias `&`. Si nosotros ejecutamos el siguiente código de ejemplo:

```cpp
cout << j << endl;
cout << i << endl;
```

Obtendremos la salida:
```
8
8
```

¿Entonces en que cambiar respecto a su código equiparable con variables primitivas? 
`int j = 8; int i = j;`

La diferencia reside al evaluar:
```cpp
i = 10;
cout << j << endl;
cout << i << endl;
```

Esperamos, que al igual que en el caso con las variables primitivas, la salida sea:
```
10
8
```

Ya que `j` se vería inalterada con el cambio de `i`. Pero la salida generada por el código con el uso de referencia, nos muestra:
```
10
10
```

Esto se debe a que al hacer la referencia `int &i = j;` se establece un alias entre `j` e `i` y a partir de ahí, ambas apuntarán a la misma dirección de memoria, por lo tanto, los cambios que se hagan por cualquiera de las dos variables, repercuten sobre la otra.

**Pregunta**
>- ¿Qué ocurrirá si declaramos una tercera referencia `h` sobre `i`? 

