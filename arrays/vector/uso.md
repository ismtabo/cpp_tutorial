## Uso de std::vector

Para poder usar estos vectores hay que incluir la librería al inicio del programa de la siguiente manera:
```cpp
#include <iostream>
#inlcude <vector>
using namespace std;

int main(){
/*code*/
}
```
Para inicializarlo dado que es una clase genérica hay que indicar el tipo de dato de la colección:

```cpp
#include <iostream>
#inlcude <vector>
using namespace std;

int main(){
    vector<int> myVector;
    vector<string> myString;
}
```
Existen múltiples posibilidades de iniciación:
```cpp
// Vector v de tipo de dato T vacío
vector<T> v;
// v2 es copia del vector v1
vector<T> v2(v1);
// Equivalente al anterior
vector<T> v2=v1;
// v tiene n valores con valor val
vector<T> v(n,val);
// v tiene n valores inicializados a un valor por
// defecto que dependerá del tipo de dato T.
// Para tipos de dato como int, double el valor es 0
vector<T> v(n);
// v inicializado con los valores x,y,z, ...
vector<T> v{x,y,z...};
// Equivalente al anterior
vector<T> v={x,y,z...};
```
