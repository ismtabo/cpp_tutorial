# Struct

<!--Es una colección de variables del mismo o distinto tipo que se referencia bajo un único nombre, proporcionando un medio eficaz de mantener junta la información relacionada.  
La definición de una estructura se realiza de la siguiente manera:-->

Un _struct_ o estructura es un conjunto de elementos agrupados bajo un mismo nombre. Cada uno de estos elementos se le considera un "miembro" de la estructura. En **C++** se declaran mediante la siguiente sintaxis:

```cpp
struct nombre {
    tipo_miembro_1 nombre_miembro1;
    tipo_miembro_2 nombre_miembro2;
    tipo_miembro_3 nombre_miembro3;
};
```

Esta característica heredada de **C** es muy útil al poder combinar distintos tipos de datos primitivos (`int`, `double`, ...), junto tipos complejos tales como `string`, bajo un nombre; permitiéndonos así, nuevos tipos abstractos de datos en nuestro código, como se va a mostrar a continuación.



