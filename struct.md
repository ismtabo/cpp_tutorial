# Struct

Es una colección de variables del mismo o distinto tipo que se referencia bajo un único nombre, proporcionando un medio eficaz de mantener junta la información relacionada.
La definición de una estructura se realiza de la siguiente manera:
```
struct  nombre {
    lista de variables
    };
```
Donde struct es la palabra clave que indica al compilador que se va a definir una estructura, nombre es el identificador de la estructura, y en lista de variables es donde se declaran las variables que van a componer esa estructura.
Ejemplo:
```cpp
struct complejo{
    double real;
    double imag;
    };
```
Definida la estructura se pueden declarar variables de ese tipo. Hay varias maneras de hacerlo:
- Directamente en la deficnión:
```
struct  nombre {
    lista de variables
    }var1, var2, var3,...;
```
- Tras la definición:
```
struct  nombre {
    lista de variables
    };
struct nombre var1, var2, var3,...
```
- Usando la sentencia *typedef*, que permite definir tipos de datos. Su uso con los structs es el siguiente:
```
typedef struct{
lista de variables
}nombre;
nombre var1, var2, var3,...
```
Para acceder a los valores de la estructura se hace de la siguiente manera:
```
nombre.miembro
```
Nombre es como hemos llamado a la variable y miembro el nombre de cualquiera de las variables declaradas *lista de variables*