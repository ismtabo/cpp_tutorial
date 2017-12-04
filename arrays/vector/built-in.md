# Built-in
Un built-in son funciones predefinidas en la clase. (`.at()` que mostramos anteriormente)

A continuación se muestran las más importantes:

| Método | Funcionalidad |
|--------|--------|
| `operator[]` o `at()` | Método empleado para acceder un elemento del vector mediante su indice |
| `front()` | Delvuelve el primer elemento del vector |
| `back()` | Devuelve el último elemento del vector |
| `size()` | Método que devuelve un valor entero que se corresponde con la cantidad de elementos en el vector |
| `empty()` | Devuelve un valor booleano que nos dice si el vector está vacío o no |
| `clear()` | Elimina todos los elementos del vector, dejándolo vacío |
| `push_back()` | Añade el elemento que se indica por parámetros al final del vector |
| `pop_back()` | Elimina el último elemento del vector |

Ejemplo de uso:
```cpp
#include <iostream>
#include <vector> // Es necesario importar la libreria
using namespace std;

int main(){
    vector<int> mi_vector;
    if(mi_vector.empty())
        cout << "El vector esta vacio\n";
    mi_vector.push_back(2);
    mi_vector.push_back(3);
    mi_vector.push_back(4);
    cout << "El numero de elementos que hay en el vector son " << mi_vector.size() <<'\n';
    cout << "El primer elemento es " << mi_vector.front() << '\n';
    cout << "El ultimo elemento es " << mi_vector.back() << '\n';
    mi_vector.pop_back();
    cout << "Ahora el ultimo elemento es " << mi_vector.back() << '\n';
    mi_vector.clear();
    cout << "Ahora el vector contiene " << mi_vector.size() << " elementos\n";
    return 0;
}
```
Para saber más, puedes consultar [documentación ofcial](http://www.cplusplus.com/reference/vector/vector/) la de
`vector`.
