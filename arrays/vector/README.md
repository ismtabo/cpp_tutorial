# std::vector
`vector`es una clase genérica que permite almacenar una colección de objetos del mismo tipo. El beneficio que aporta, frente a los arrays de **C**, es que `vector` te permite tener un a longitud dinámica.

El funcionamiento de esta clase consiste en memoria dinámica y recolocando el vector en memoria para aumentarlo de tamaño. Con el fin de evitar costes de recolocación cada vez que añades un elemento se inicializa de un tamaño mayor, solo teniendo que recolocarse en memoria cuando se llenen.
