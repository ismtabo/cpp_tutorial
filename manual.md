Introducción a C++
====

Contenidos

Introducción
----
<small><small>[(Arriba)](#)</small></small>

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

Compiladores
----
<small><small>[(Arriba)](#)</small></small>
Un **compilador** es un programa informático que traduce un programa escrito en un lenguaje de alto nivel al lenguaje del ordenador.

Para aquellos que ya habéis trabajado con otros lenguajes compilados como **C** o **Java**, estaréis familiarizados con esto. Compilar un programa de **C++** no es muy distinto, supongamos el siguiente código ejemplo de nuestro archivo `helloworld.cpp`. Por fortuna es nuestro conocido _"Hello World"_ en **C++**.
```cpp
// mi primer programa en C++
#include <iostream>

int main()
{
  std::cout << "Hello World!";
}
```

Para compilar este programa tenéis varias posibilidades según el sistema operativo sobre el que trabajéis estas son las opciones:

| Compilador | Instrucción |
|--------|--------|
| **GCC** | `$ g++ -std=c++0x helloworld.cpp -o HelloWorld` |
| **Clang** | `$ clang++ -std=c++11 -stdlib=libc++ helloworld.cpp -o HelloWorld` |

_Opciones especiales_:
- `-std=.`: Esta opción nos ofrece usar un estandar u otro para compilar. Por ejemplo `-std=c++11` en el caso de usar declaraciones o sentencias especiales de este estandar, como veremos más adelante.
- `-o`: nos deja elegir el nombre del ejecutable del programa compilado.

Estos compiladores también están integrados en diversos IDEs que facilitan la programación. Tales como:

| **IDE** | **Plataforma** |
|--------|--------|
| [**Code::blocks**](http://www.codeblocks.org/) | Windows/Linux/MacOS |
| [**Visual Studio Express**](https://www.visualstudio.com/en-us/products/visual-studio-express-vs.aspx) | Windows |
| [**Dev-C++**](http://sourceforge.net/projects/orwelldevcpp/) | Windows |
| [**Sublime 2/3**](https://www.sublimetext.com/) | Windows/Linux/MacOS |
| [**Atom**](https://atom.io/) | Windows/Linux/MacOS |


Estructura de un programa
----
<small><small>[(Arriba)](#)</small></small>
Revisemos el código anterior:
```cpp
// mi primer programa en C++
#include <iostream>

int main()
{
  std::cout << "Hello World!";
}
```
Salida:
```bash
Hello World
```

Las estructuras del programa que podemos ver son las siguientes:
- `// mi primer programa en C++`: `//` indica que la línea es un comentario
- `#include <iostream>`: Esta línea que comienza con un `#` indica que es una línea que procesa el compilador. La directiva `#include <iostream>` hace que la biblioteca `iostream` se tenga en cuenta en la compilación del programa.
- `int main()`: Declaración de una función, en este caso es la función `main`, al igual que en **C** esta función es la que se ejecuta en primer lugar. Entre los `()` se declaran de forma opcional los parámetros.
- `{` and `}`: las respectivas líneas #5 `{` y #7 `}` indican el inicio y final de la declaración de un conjunto de sentencias dentro de una función.
- `std::cout << "Hello World!";` : declaración de operación.


Tipos de datos
----
<small><small>[(Arriba)](#)</small></small>
Como en la mayoría de los lenguajes el operador para la declaración de variables es el `=`.
```cpp
a = 5;
b = 2;
a = a-1;
result = a - b;
```
El tipado de **C++** el tipado es **fuerte**, **estático** y **nominativo**. Recordando, esto significa que _no se pueden usar una variable definida con un tipo concreto como si fuera de otro distinto_(_fuerte_), _una vez declarado el tipo de una variable este no puede cambiar_ (_estático_) y _los tipos de las variables son declaradas por el programador_ (_nominativo_).

###Tipos fundamentales

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

####Asignaciones

Declaración y operaciones sobre variables
```cpp
#include <iostream>
using namespace std;

int main ()
{
  // declaración de variables:
  int a, b;
  int result;

  // operaciones:
  a = 5;
  b = 2;
  a = a + 1;
  result = a - b;

  // impriendo el resultado:
  cout << result;

  // finalización del problema:
  return 0;
}
```
Salida
```bash
4
```

En el caso anterior hemos dado un ejemplo en el que operamos con las distintas variables declaradas. Como has podido observar hemos operado sobre enteros y luego hemos imprimido por pantalla el resultado.

>- ¿Cómo harías para operar sobre tipos de coma flotante?
>- ¿Es posible sumar un entero a un float, o a un caracter?¿Cuál es el resultado final?

####Inicialización

Hemos visto que para inicializar una variable se hace uso de la declaración:
```cpp
int x = 0;
```

Pero existen más opciones. Como son las sentencias:
```cpp
int x(0);// no confundir con la declaración de funciones 
int x{0};
```
**Aviso**: _Este último inicializador sólo está disponible con el estandar `C++11`, esto significa que para compilarlo necesitaremos usar la opción `-std=c++11`._

Código de ejemplo:
```cpp
// inicialización de variables

#include <iostream>
using namespace std;

int main ()
{
  int a=5;               // valor inicial: 5
  int b(3);              // valor inicial: 3
  int c{2};              // valor inicial: 2
  int result;            // valor inicial sin determinar

  a = a + b;
  result = a - c;
  cout << result;

  return 0;
}
```
Salida
```bash
6
```

>- Modifique el ejemplo anterior para que a, b, y c sean variables de punto flotante inicializadas en 5.0, 3.4, 2.11
>- Pruebe si puede utilizarse para inicializar caracteres.

####Deducción de tipo
Como punto final para explicar los tipos fundamentales, ahora vamos a ver como un tipo puede deducir el tipo de la variable que se le asigna. Estas son las declaraciones `auto` y `decltype(foo)`.

Ejemplos de uso:
```cpp
int a = 0;
auto foo = a;  // mismo resultado que: int bar = foo;
decltype(a) bar;  // mismo resultado que: int bar; 
```

####Strings

Los string representan un conjunto ordenado de caracteres, literalmente, _una cadena_. En **C++** nos encontramos con la clase _string_ la cual nos permite guardar esa secuencia de caracteres.

La primera diferencia con los tipos que hemos ido viendo hasta ahora, es que esta clase necesita importar su código desde su propia biblioteca estandar `<string>`, por lo tanto deberemos incluirla en la cabecera de nuestro programa. A diferencia de **C**, a los strings no se les trata como un array de caracteres terminado por `\0`, por lo tanto cuando los declaremos no será necesario declararlo como `char cadena[]`, ni reservar un espacio de más para nuestro carácter de finalización.

```cpp
#include <iostream>
#include <string>
using namespace std;

int main ()
{
  string mistring;
  mistring = "Esto es un string";
  cout << mistring;
  return 0;
}
```
Salida
```bash
This is a string
```

Como hemos visto en el ejemplo anterior, los string se declaran y se le asignan valores de igual forma que los anteriores tipos. 

> - Pruebe a asignar nuestra variable `mistring` el valor `Esto es una cadena`, e imprimirlo por pantalla.
> - Inicialice dos nuevos string `cadena` y `caracteres`, mediante los operadores de inicialización `( . )` y `{ . }` que hemos visto con anterioridad.

#####Operaciones con clase string

Como pensarás la clase string tiene más operaciones que la asignación, veamos una pequeña introducción a las capacidades de esta clase.

```cpp
#include <iostream>
#include <string>
using namespace std;

int main ()
{
  string name ("Juan");
  string family ("García");
  name += " K. ";         // c-string
  name += family;         // string
  name += '\n';           // character

  cout << name;
  return 0;
}
```
> ¿Cuál será la salida del programa anterior?

El operador `+=` sobre un string añadira el c-string, string o carácter que indiquemos al final del string. También se puede añadir mediante el operador `.append( . )`.

> Modifique el código de ejemplo anterior reemplazando el operador `+=` con el operador de clase `.append( . )` 

Más operadores de la clase `string`:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main ()
{
  string name ("Juan");

  cout<<name.at(0)<<endl;
  cout<<name.size()<<endl;
  return 0;
}
```
> ¿Qué salida esperamos en el código anterior?

Operadores de acceso a un elemento: `.at(.)`, `[.]`, `.back()`, `.front()`.
Operadores para conocer el tamaño del string: `.size()`, `.length()`

Más información: [referencia](http://www.cplusplus.com/reference/string/string/)

###Constantes

Constantes son aquellos valores que están fijados, en **C++** se encuentran los siguientes tipos.

####Literales

Los literales son constante que expresan un valor particular. Como vimos antes, para asignar un valor a una variable lo declarabamos de la siguiente manera:
`a = 5`
El `5` en este código es el _literal constante_ que expresa en código fuente el valor que queremos darle. Los literales constantes están clasificados en los siguientes tipos:
- **Enteros**(_Integer_):
	
    | Tipo | Ejemplo | sufijo |
|--------|--------|
|    decimal    |   75     |
| octal | 0113 |
| hexadecimal | 0x04b |
| _int_ | 75 |
| _unsigned int_  | 75u | `u`
| _long_ | 75l | `l`
| _unsigned long_ | 75ul ó 75lu | `ul` o `lu`

- **Punto flotante**(_Floating Point_): 
	```cpp
3.14159    // 3.14159
6.02e23    // 6.02 x 10^23
1.6e-19    // 1.6 x 10^-19
3.0        // 3.0
    ```
	| Tipo | Ejemplo | Sufijo |
|--------|--------|
|    _float_    |    6.02e23f    | `f` o `F` |
| _long double_ | 3.14159L | `l` o `L` |

- **Caracteres y string**: 
	```cpp
'z'
'p'
"Hello world"
"How do you do?"
    ```
    Conjunto de cadenas:
    ```cpp
"this forms" "a single"     " string "
"of characters"
```
Es similar a 
```cpp
"this formsa single string of characters"
```
Cadenas separadas en dos líneas:
```cpp
x = "string expressed in \
two lines"
```
Es similar a
```cpp
x = "string expressed in two lines"
```
    - Caracteres de escape
  | Escape code | Description |
  | ---- | ----- |
| \n | newline 
| \r | carriage return
| \t | tab
| \v | vertical tab
| \b | backspace
| \f | form feed (page feed)
| \a | alert (beep)
| \' | single quote (')
| \" | double quote (")
| \? | question mark (?)
| \\ | backslash (\)
	- Prefijos especiales:
		- Caracteres:
	| Prefijo | Tipo | 
|--------|--------|
|    u    |    _char16_t_    |
| U | _char32_t_ |
| L | _wchar_t_ |
		- String:
		| Prefjo | Descripción | Ejemplo |
|--------|--------|
| u8 | Literal codificado en UTF-8 |
| R | _raw strin_ | `R"(string with \backslash)"` |
- Otros literales:
	```cpp
bool foo = true;
bool bar = false;
int* p = nullptr;
```

####Expresiones tipadas constantes
A veces es conveniente dar un nombre a un valor constante:

```cpp
#include <iostream>
using namespace std;

// Expresiones constantes
const double pi = 3.14159;
const char newline = '\n';

int main ()
{
  double r=5.0;               // radius
  double circle;

  circle = 2 * pi * r;
  cout << circle;
  cout << newline;
}
```

####Definiciones del preprocesador (_#define_)
También puede hacerse uso del preprocesador para crear variables constantes mediante la sentencia:
`#define identifier replacement`
Esto hace que el **preprocesador** interprete las coincidencias de `identifier` por `replacement`.

```cpp
#include <iostream>
using namespace std;

#define PI 3.14159
#define NEWLINE '\n'

int main ()
{
  double r=5.0;               // radius
  double circle;

  circle = 2 * PI * r;
  cout << circle;
  cout << NEWLINE;

}
```

Como `#include` las sentencias `#define` son directivas del **preprocesador** y no necesitan `;`.

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


