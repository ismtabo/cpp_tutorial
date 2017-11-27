# Llamadas a funciones

Las funciones pueden ser llamadas desde cualquier punto de un programa.

La llamada de una función se produce mediante el uso de su nombre en una sentencia, pasando una lista de argumentos que deben coincidir en número y tipo con los especificados en la declaración, en caso contrario se produciría una conversión de tipos cuyos resultados pueden no ser los esperados. En general, los parámetros se pueden pasar por valor (copia el valor de la variable que le pasamos) y por referencia, usando en este caso **punteros** (dirección de memoria donde se almacena la variable), que serán vistos más adelante. En este último caso será posible modificar el valor de la variable usada en la llamada.

Ejemplo:
```cpp
#include <iostream>
using namespace std;
//Función que retorna un número
int numero(); 
//Función que imprime una cuenta atrás
void cuentaAtras(int n);

int main ()
{
  int c = numero();
  cuentaAtras(c);
  cout << "¡Despegue!\n";
}

int numero()
{
  return 10;
}

void cuentaAtras(int n)
{
  for(int i=n;i>0;i--){
    cout << n << ", ";
  }
}
```

**Pregunta**
>- ¿Qué ocurrirá si llamo a cuentaAtras así `cuentraAtras(numero())`? 