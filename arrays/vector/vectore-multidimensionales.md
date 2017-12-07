# Vectores multidimensionales

Al igual que con los _arrays_, con los vectores también se pueden tener más de una dimensión. Pero existe una clara diferencia respecto a estos primeros.

Utilizando la genericidad de la clase `std::vector`, para definir un vector de dos dimensiones --ejemplo básico con los _arrays_ multidimensionales--, utilizaremos el tipo `vector<int>` para cada uno de los elementos de nuestro vector matricial. Es decir:

```cpp
vector<vector<int>> matrix;
```

Esta declaración tiene sentido, ya que al igual que para los _arrays_ multidimensionales teníamos _arrays_ de _arrays_, aquí tendremos vectores de vectores.

Tomando el ejemplo de una matriz veremos las distintas funcionalidades que tiene la multidimensionalidad en los vectores, y como trabajar con ello.

## Inicialización

Ya hemos visto un ejemplo de la declaración de un vector de dos dimensiones. Al igual que con los vectores de una dimensión, podrémos inicializar la matriz mediante las siguientes expresiones: 
```cpp
// v with n elements of default value of T. 
// For int type, default value is 0.
std::vector<std::vector<int> > v(
    n,
    std::vector<int>(m));
// v with n vectors of m elements with value equals to val
std::vector<std::vector<int> > v(
    n,
    std::vector<int>(m, val));
    
// With standard c++11 or above:
// v initialize with vectors x, y, z, ...
std::vector<std::vector<int> > v { v1, v2 };
// v initialize with: vectors of elements {a, b, c}, vector with elemnts {d, e, f}, ...
std::vector<std::vector<int> > v { { a, b, c }, { d, e, f } };
```

## Acceso a elementos

Dado que lo que vamos a tener son vectores de vectores, para acceder a los datos, hay que tener en cuenta que el operador `[·]` y la función `.at(·)` sobre las primeras dimensiones nos devolverá objetos de tipo `vector`, por lo que tendremos que tener cuidado con los tipos en dichos casos.

```cpp
matrix.at(0); // Returns vector which correspond to row 0
matrix.at(0).at(0); // Returns elemento at first position of the first vector
```

## Referencias, punteros y funciones

Para el uso de referencias, puntero o el uso como parámetros de funciones respecto a vectores unidimensionales, no cambia respecto a los vectores unidimensionales, pensando que el tipo genérico `T`, donde antes era un tipo simple, ahora es `std::vector<T>`.
