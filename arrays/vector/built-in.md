# Métodos y Funciones de `vector`


Alguna de las funciones más importantes de `vector`:

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
    vector<int> my_vector;
    if(my_vector.empty())
        cout << "El vector esta vacio\n";
    my_vector.push_back(2);
    my_vector.push_back(3);
    my_vector.push_back(4);
    cout << "El numero de elementos que hay en el vector son " << my_vector.size() <<'\n';
    cout << "El primer elemento es " << my_vector.front() << '\n';
    cout << "El ultimo elemento es " << my_vector.back() << '\n';
    my_vector.pop_back();
    cout << "Ahora el ultimo elemento es " << my_vector.back() << '\n';
    my_vector.clear();
    cout << "Ahora el vector contiene " << my_vector.size() << " elementos\n";
    return 0;
}
```
Para saber más, puedes consultar [documentación ofcial](http://www.cplusplus.com/reference/vector/vector/) la de
`vector`.
