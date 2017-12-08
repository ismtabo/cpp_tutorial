# Acceso a los elementos
Una vez que hemos creado el vector, podemos acceder a los elementos con los corchetes cuadrados (como un array normal) o usando la función predefinida `.at`, de la clase `vector`, con el índice del elemento como parámetro:
```cpp
#include <iostream>
#include <vector>
using namespace std;
int main()
{
    vector<int> myVector(3,4);
    cout<< "My index is "<< 2 << ", my value is "<< myVector[2]<<endl;

    cout<< "My index is "<< 2 << ", my value is "<< myVector.at(2)<<endl;
    
```
Como hemos visto ambas formas de acceder al vector funciona, pero es preferible usar `.at` tiene implementado un control de acceso para impedir que nos salgamos del rango del vector.

El contenedor ```vector```  permite añadir elementos de forma dinámica con la función ```push_back(type variable)```.

Ejemplo: Añadir los valores 0 al 9 a un vector inicialmente vacío.
```cpp
#include <iostream>
#include <vector>
using namespace std;
int main()
{
    vector<int> v;             // Empty vector of integers
    for(int i=0; i!=10; ++i)
        v.push_back(i);        // Add i element at each iteration
    // Prints values from 0 to 9
    for(int i=0; i!=10; ++i)
        cout<<v[i]<<" ";       // Access to values as in arrays
    cout<<endl;
}
```
