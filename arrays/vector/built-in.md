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
        cout << "Vector is empty\n";
    my_vector.push_back(2);
    my_vector.push_back(3);
    my_vector.push_back(4);
    cout << "Number of elements in my_vector: " << my_vector.size() << endl;
    cout << "First element: " << my_vector.front() << endl;
    cout << "Last element: " << my_vector.back() << endl;
    my_vector.pop_back();
    cout << "Pop last element of vector" << endl
    cout << "Last element: " << my_vector.back() << endl;
    my_vector.clear();
    cout << "Number of elements in my_vector " << my_vector.size() << endl;
    return 0;
}
```
Para saber más, puedes consultar [documentación ofcial](http://www.cplusplus.com/reference/vector/vector/) la de
`vector`.
