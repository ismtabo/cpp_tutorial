# Declaración de una función

Toda función debe ser definida antes de ser usada, al igual que las variables. Por convenio, estas son definidas después de la función `main`, por lo que son necesarias los **prototipos** de las funciones(*cabeceras*) que ayuden al compilador para saber la forma de dicha función. La estructura de un prototipo es la siguiente:

```cpp
type name (type_param1, type_param2[, ...]);
```

Como puede observarse, no es necesario incluir el nombre de cada parámetro, únicamente hay que definir su tipo, aunque se puede añadir, tal que la estructura sea la siguiente:

```cpp
type name (type_param1 param1, type_param2 param2[, ...]);
```
