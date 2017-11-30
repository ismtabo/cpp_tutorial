# Uso de _Structs_

Al igual que para C, para C++ `struct` es la palabra clave que indica al compilador que se va a definir una estructura.

Para su definición, tal como dijimos en la página anterior hay que dar un nombre identificador a la estructura, y en lista de variables que vayan a estar agrupadas en las estructuras tal como se muestra a continuación.  
Ejemplo:

```cpp
struct complex{
    double real;
    double imag;
};
```

Esta estructura de _complex_ tiene dos miembros _real_ e _imag_, con tipo `double` en ambos casos. De esta manera si nosotros quiesiesemos declarar el número complejo _1+1i_ lo haríamos como se expone en el código siguiente:

```cpp
complex complejo;
complejo.real = 1;
complejo.img = 1;
```

Pudiendo acceder a cada uno de los miembros mediante notación doteada:

```cpp
cout << complejo.real;  // 1
cout << complejo.img;   // 1
```

Al definir un _struct_ puede utilizarse también como tipo de los parámetros de una función, tanto para la cabecera, como para la definición de la variable.

```cpp
int a_polar(complex);

int a_polar(complex complejo){
    ...
    return 0;
}
```
