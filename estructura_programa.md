Estructura de un programa
====

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

