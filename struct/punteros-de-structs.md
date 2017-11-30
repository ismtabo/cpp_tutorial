# Punteros de _Structs_

Al inicio de la sección vimos como podíamos acceder a los miembros de un `struct` mediante el siguiente código:

```cpp
struct complex{
    double real;
    double imag;
};

complex complejo;
complejo.real = 1;
complejo.img = 1;

cout<<complejo.real;    // 1
cout<<complejo.img;     // 1
```

Pero al igual que en _C_, no tenemos el mismo comportamiento cuando tratamos con puntero. Para ello, en vez de notación punteada hay que utilizar el operador `->`. En el siguiente código se expone un ejemplo de cómo y cuándo debemos utilizar este operador.

```cpp
complex *ptr_complejo;
ptr_complejo = &complejo;

// Sobre variable directa:
// cout<<complejo.real;         // 1
// cout<<complejo.img;          // 1
// Sobre puntero:
cout << ptr_complejo->real;     // 1
cout << ptr_complejo->img;      // 1
```

