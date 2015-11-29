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

