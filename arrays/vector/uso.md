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
El contenedor ```vector```  permite añadir elementos de forma dinámica con la función ```push_back(type variable)```

Ejemplo: Añadir los valores 0 al 9 a un vector inicialmente vacío.
```cpp
#include <iostream>
#include <vector>
using namespace std;
int main()
{
    vector<int> v; //vector vacío de enteros
    for(int i=0; i!=10; ++i)
        v.push_back(i); // Añade de forma progresiva
    // los valores del 0 al 9
    for(int i=0; i!=10; ++i)
        cout<<v[i]<<" ";//Acceso a los elementos como en C
    cout<<endl;
}
```

