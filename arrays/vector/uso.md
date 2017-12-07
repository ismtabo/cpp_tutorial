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
// Empty vector v of type T
vector<T> v;
// v2 copy of vector v1
vector<T> v2(v1);
// Equivalent to sample above
vector<T> v2=v1;
// v with n elements with value equals to val
vector<T> v(n,val);
// v with n elements of default value of T. 
// For int type, default value is 0.
vector<T> v(n);
// v initialize with elements x, y, z, ...
vector<T> v{x,y,z...};
// Equivalent to sample above
vector<T> v={x,y,z...};
```
