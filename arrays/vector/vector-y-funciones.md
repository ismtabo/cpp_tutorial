# Vector como argumento de funciones
Al igual que los vectores de **C**, un contenedor `vector` puede pasarse por valor o por referencia.

Es preferible realizar el paso por referencia, debido a que al pasar por valor se realizaría una copia de todo el contenedor. Si tiene muchos elementos el proceso llevaría un tiempo considerable.

Una excelente práctica de programación es calificar como de tipo `const` aquellos argumentos que sean referencias pero que no deseemos modificar. Si modificamos la referencia el compilador nos avisará.

Ejemplo paso por valor:

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
  vector<int> my_vector;
  initializeVector(my_vector, 5);
  printVector(my_vector, 5);
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

Ejemplo paso por referencia:

```cpp
#include <iostream>
#include <vector>
using namespace std;

/*Function which initialize vector*/
void initializeVector(vector<int>&, int);

/*Function which prints vector at stdout*/
void printVector(const vector<int>&);

int main ()
{
  vector<int> my_vector;
  initializeVector(my_vector, 5);
  printVector(my_vector, 5);
  return 0;
}

void initializeVector(vector<int>& x, 5)
{
  for(int i=0; i< tam; i++)
     x.push_back(i);
}

void printVector(const vector<int>& x)
{
  for(int i: x)
    cout<< i << " ";
  cout << '\n';
}
```



**Pregunta**
>- ¿Por qué el la función `initializeVector` usamos paso por referencia y en `printVector` usamos paso por referencia con el modificador `const`?
