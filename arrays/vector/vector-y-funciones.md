# Vector como argumento de funciones
Al igual que los vectores de **C**, un contenedor `vector` puede pasarse por valor o por referencia.

El paso por referencia es preferido dado que en el paso por valor debemos realizar una copia de todo el contenedor. Si tiene muchos elementos el proceso llevaría un tiempo considerable.

Una excelente práctica de programación es calificar como de tipo `const` aquellos argumentos que sean referencias pero que no deseemos modificar. Si modificamos la referencia el compilador nos avisará.

Ejemplo paso por valor y referencia:

```cpp
#include <iostream>
#include <vector>
using namespace std;

/*Función de inicialización del array*/
void icicalizarArray(vector<int>& x, int tam); //paso por referencia

/*Función para imprimir el array*/
void imprimirArray(vector<int> x, int tam);//paso por valor

int main ()
{
 int vector[5];
 icicalizarArray(vector, 5);
 imprimirArray(vector, 5);
 return 0;
}

void icicalizarArray(vector<int>& x, int tam)//paso por referencia
{
 int contador=0;
 for(int i=0; i< tam; i++)  {
    x[i]=i;
  }
}

void imprimirArray(vector<int> x, int tam)//paso por valor
{
 for(int i=0; i< tam; i++)  {
    cout<< x[i]<< " ";
  }
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
