# Compiladores

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
| --- | --- |
| **GCC** | `$ g++ -std=c++11 helloworld.cpp -o HelloWorld` |
| **Clang** | `$ clang++ -std=c++11 -stdlib=libc++ helloworld.cpp -o HelloWorld` |

_Opciones especiales_:

* `-std=.`: Esta opción nos ofrece usar un estandar u otro para compilar. Por ejemplo `-std=c++11` en el caso de usar declaraciones o sentencias especiales de este estandar, como veremos más adelante.
* `-o`: nos deja elegir el nombre del ejecutable del programa compilado.

Estos compiladores también están integrados en diversos IDEs que facilitan la programación. Tales como:

| **IDE** | **Plataforma** |
| --- | --- |
| [**Code::blocks**](http://www.codeblocks.org/) | Windows/Linux/MacOS |
| [**Visual Studio Express**](https://www.visualstudio.com/en-us/products/visual-studio-express-vs.aspx) | Windows |
| [**Dev-C++**](http://sourceforge.net/projects/orwelldevcpp/) | Windows |
| [**Sublime 2/3**](https://www.sublimetext.com/) | Windows/Linux/MacOS |
| [**Atom**](https://atom.io/) | Windows/Linux/MacOS |
| [**Visual Studio Code**](https://code.visualstudio.com) | Windows/Linux/MacOS |
| [**Clion**](https://www.jetbrains.com/clion/) | Windows/Linux/MacOS |



