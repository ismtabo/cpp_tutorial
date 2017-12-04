# std::vector
```vector```es una clase genérica que permite almacenar 
una colección de objetos del mismo tipo. El beneficio que aporta, frente a los arrays de **C**, es que no es necesario conocer el tamaño de estos, puesto que pueden aumentar de tamaño dejando el control del tamaño al contenedor automáticamente. 

El funcionamiento de esta clase se basa en memoria dinámica y recolocando el vector en memoria para aumentarlo de tamaño. Con el fin de evitar costes de recolocación cada vez que añades un elemento se inicializa de un tamaño mayor, solo teniendo que recolocarse en memoria cuando se llenen.
