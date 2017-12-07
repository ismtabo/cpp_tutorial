# Uso de _Structs_

Al igual que para **C**, para **C++** `struct` es la palabra clave que indica al compilador que se va a definir una estructura.

Para su definición, tal como dijimos en la página anterior hay que dar un nombre identificador a la estructura, y en lista de variables que vayan a estar agrupadas en las estructuras tal como se muestra a continuación.  
Ejemplo:

```cpp
struct Complex_t{
    double r;
    double i;
};
```

Esta estructura de _complex_ tiene dos miembros _real_ e _imag_, con tipo `double` en ambos casos. De esta manera si nosotros quiesiesemos declarar el número complejo _1+1i_ lo haríamos como se expone en el código siguiente:

```cpp
Complex_t complex;
complex.r = 1;
complex.i = 1;
```

Pudiendo acceder a cada uno de los miembros mediante notación doteada:

```cpp
cout << complex.r;  // 1
cout << complex.i;   // 1
```

Al definir un _struct_ puede utilizarse también como tipo de los parámetros de una función, tanto para la cabecera, como para la definición de la variable.

```cpp
int magnitude(Complex_t);

/* Main */
// ...

int magnitude(Complex_t complex){
    ...
}
```
