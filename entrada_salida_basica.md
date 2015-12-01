Entrada y salida básica
====

Lo visto hasta ahora nos ha permitido asignar variables y operar entre ellas, pero también queremos interactuar con el usuario, y esto lo vamos a conseguir mediante entrada y salida básica. 

**C++** abstrae mediante _streams_ las operaciones de entrada y salida a partir de sistemas como la pantalla, el teclado o un fichero. Un _stream_ es una entidad donde el programa puede insertar y extraer caracteres. Debemos tener en cuenta que este flujo de origen y destino de caracteres se hace de forma secuencial.

La biblioteca correspondiente a la entrada y salida es `iostream`. Esta contienen las siguientes instancias _stream_ según el objetivo de la itneacción:

| **stream** | **description** |
|------------|-----------------|
| `cin` | Estandar _stream_ de entrada |
| `cout` | Estandar _stream_ de salida |
| `cerr` | Estandar _stream_ de salida de error|
| `clog` | Estandar _stream_ de salida de log |

Como observamos hay dos principales instancias `cin` y `cout` que son los métodos estandar de entrada y salida. También encontramos dos especializaciones de salida `cerr` y `clog` que se comportan de manera similar a la la salida estandar pero con sus peculiaridades que más adelante explicaremos.




