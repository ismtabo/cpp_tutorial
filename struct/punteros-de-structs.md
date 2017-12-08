# Punteros de _Structs_

Al inicio de la sección vimos como podíamos acceder a los miembros de un `struct` mediante el siguiente código:

```cpp
struct Complex_t{
    double r;
    double i;
};

Complex_t complex;
complex.r = 1;
complex.i = 1;

cout<<complex.r;    // 1
cout<<complex.i;    // 1
```

Pero al igual que en _C_, no tenemos el mismo comportamiento cuando tratamos con puntero. Para ello, en vez de notación punteada hay que utilizar el operador `->`. En el siguiente código se expone un ejemplo de cómo y cuándo debemos utilizar este operador.

```cpp
Complex_t *ptr_complex;
ptr_complex= &complex;

// Using variable complex:
// cout<<complejo.r;          // 1
// cout<<complejo.i;          // 1

// Using pointer to complex:
cout << ptr_complex->r;       // 1
cout << ptr_complex->i;       // 1
```
