# Vector como argumento de funciones
Al igual que los vectores de **C**, un contenedor `vector` puede pasarse por valor o por referencia.

Es preferible realizar el paso por referencia, debido a que al pasar por valor se realizaría una copia de todo el contenedor. Si tiene muchos elementos el proceso llevaría un tiempo considerable.

Una excelente práctica de programación es calificar como de tipo `const` aquellos argumentos que sean referencias pero que no deseemos modificar. Si modificamos la referencia el compilador nos avisará.

Ejemplo paso por valor y referencia:

```cpp
#include <iostream>
#include <vector>
using namespace std;

/*Function which initialize vector*/
void initializeVector(vector<int>&, int);

/*Function which prints vector at stdout*/
void printVector(vector<int>);

int main ()
{
  vector<int> int_vector;
  initializeVector(vector, 5);
  printVector(vector, 5);
  return 0;
}

void initializeVector(vector<int> x, 5)
{
  for(int i=0; i< tam; i++)
     x.push_back(i);
}

void printVector(vector<int> x)
{
  for(int i: x)
    cout<< i << " ";
  cout << '\n';
}
```

Ejemplo con const:

```cpp
#include <iostream>
#include <vector>
using namespace std;

/*Función de inicialización del array*/
void icicalizarArray(vector<int>& x, int tam);

/*Función para imprimir el array*/
void imprimirArray(const vector<int>& x, int tam);

int main ()
{
 int vector[5];
 icicalizarArray(vector, 5);
 imprimirArray(vector, 5);
 return 0;
}

void icicalizarArray(vector<int>& x, int tam)
{
 int contador=0;
 for(int i=0; i< tam; i++)  {
    x[i]=i;
  }
}

void imprimirArray(const vector<int>& x, int tam)
{
 for(int i=0; i< tam; i++)  {
    cout<< x[i]<< " ";
  }
  cout << '\n';
}
```

**Pregunta**
>- ¿Por qué el la función `icicalizarArray` usamos paso por referencia y en `imprimirArray` usamos paso por referencia con el modificador `const`?
