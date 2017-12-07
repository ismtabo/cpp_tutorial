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

## Inicialización 

Para inicializar un _struct_ en **C** según se definía, se podía hacer mediante el siguiente código:
```cpp
struct Complex_t complex = {1, 1};
struct Complex_t complex = {.r = 1, .i = 1}; // With member name asociation
```

En **C++** se inicializan según se definen de la misma forma, sin la necesidad de la palabra reservada `struct` antes del tipo de la variable, es decir:
```cpp
Complex_t complex = {1, 1};
Complex_t complex = {.r = 1, .i = 1}; // With member name asociation
```
Aunque por retrocompatibilidad, también se puede utilizar la inicialización de **C**.

A partir del estándar *C++11* tambien es posible la inicialización tal y como hacíamos para los tipos de datos primitivos, mediante:
```cpp
Complex_t complex {1, 1};
Complex_t complex {.r = 1, .i = 1}; // With member name asociation
```

**Aviso**: 
- No es necesario inicializar un _struct_ según se define. 
- La sintáxis de inicialización es válida para asignar nuevos valores, únicamente con estándares **C++11** o posteriores. 
- En la sintáxis de inicilización utilizando los nombres de los miembros es necesario utilizar el mismo orden que en la definición del _struct_.

## Escritura y lectura de los miembros
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

## _Struct_ como parámetros
Al definir un _struct_ puede utilizarse también como tipo de los parámetros de una función, tanto para la cabecera, como para la definición de la variable.

```cpp
int magnitude(Complex_t);

/* Main */
// ...

int magnitude(Complex_t complex){
    ...
}
```

## Referencias de _Structs_

Al igual que con otros tipos, se pueden realizar referencias a _struct_ que tendrían el mismo acceso y uso que los alias a otros tipos.
```cpp
Complex_t &ref_complex = complex;
ref_complex.r = 1;
ref_complex.i = 1;

cout<<complex.r;    // 1
cout<<complex.i;    // 1
```

## Colecciones de _Structs_

También se pueden generar arrays y vectores de _structs_ indicando el nombre del tipo en la declaración de dicho array o _struct_.

```cpp
Complex_t complex_array[10];      // Array of 10 complex numbers
vector<Complex_t> complex_vector; // Vector of complex numbers
```


