# Vector como argumento de funciones
Al igual que los vectores de **C**, un contenedor `vector` puede pasarse por valor o por referencia.

El paso por referencia es preferido dado que en el paso por valor debemos realizar una copia de todo el contenedor. Si tiene muchos elementos el proceso llevaría un tiempo considerable.

Una excelente práctica de programación es calificar como de tipo `const` aquellos argumentos que sean referencias pero que no deseemos modificar. Si modificamos la referencia el compilador nos avisará.