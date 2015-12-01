_stringstream_
====

`<sstream>` define un tipo llamado `stringstream` que nos permite tratar un string como un stream, eso nos permite la inserción y la extracción desde y a strings de la misma manera que podríamos hacer con `cin` y `cout`. De forma que podríamos extraer de un string:

```cpp
string mystr ("1204");
int myint;
stringstream(mystr) >> myint;
```