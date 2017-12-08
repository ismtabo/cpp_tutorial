# Struct

Un _struct_ o estructura es un conjunto de elementos agrupados bajo un mismo nombre. Cada uno de estos elementos se le considera un **miembro** de la estructura. En **C++**, las plantillas de estructuras se declaran mediante la siguiente sintaxis:

```cpp
struct name {
    type_member_1 member1;
    type_member_2 member2;
    type_member_3 member3;
    ...
};
```

Esta característica heredada de **C** es muy útil al poder combinar distintos tipos de datos primitivos (`int`, `double`, ...), junto tipos complejos tales como `string`, bajo un nombre; permitiéndonos así, nuevos tipos abstractos de datos en nuestro código, como se va a mostrar a continuación. 

`name` representa la _etiqueta_ que se da a la estructura, con la que se podrá nombrar en posteriores usos.
