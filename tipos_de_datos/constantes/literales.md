Constantes
====

Constantes son aquellos valores que están fijados, en **C++** se encuentran los siguientes tipos.

Literales
----

Los literales son constante que expresan un valor particular. Como vimos antes, para asignar un valor a una variable lo declarabamos de la siguiente manera:
`a = 5`
El `5` en este código es el _literal constante_ que expresa en código fuente el valor que queremos darle. Los literales constantes están clasificados en los siguientes tipos:

###**Enteros**(_Integer_)
	
| Tipo | Ejemplo | sufijo |
|--------|--------|----|
|    decimal    |   75     ||
| octal | 0113 ||
| hexadecimal | 0x04b ||
| _int_ | 75 ||
| _unsigned int_  | 75u | `u`|
| _long_ | 75l | `l`|
| _unsigned long_ | 75ul ó 75lu | `ul` o `lu`|

###**Punto flotante**(_Floating Point_)

```cpp
3.14159    // 3.14159
6.02e23    // 6.02 x 10^23
1.6e-19    // 1.6 x 10^-19
3.0        // 3.0
```
    
| Tipo | Ejemplo | Sufijo |
|--------|--------|----|
|    _float_    |    6.02e23f    | `f` o `F` |
| _long double_ | 3.14159L | `l` o `L` |

###**Caracteres y string**

```cpp
'z'
'p'
"Hello world"
"How do you do?"
```
    
Conjunto de cadenas:

```cpp
"this forms" "a single"     " string "
"of characters"
```

Es similar a 
```cpp
"this formsa single string of characters"
```

Cadenas separadas en dos líneas:

```cpp
x = "string expressed in \
two lines"
```

Es similar a

```cpp
x = "string expressed in two lines"
```

####Caracteres de escape
    
| Escape code | Description |
| ---- | ----- |
| \n | newline |
| \r | carriage return |
| \t | tab |
| \v | vertical tab |
| \b | backspace |
| \f | form feed (page feed) |
| \a | alert (beep) |
| \' | single quote (') |
| \" | double quote (") |
| \? | question mark (?) |
| \\ | backslash (\) |
    
####Prefijos especiales

#####Caracteres

| Prefijo | Tipo | 
|--------|--------|
| u | _char16_t_ |
| U | _char32_t_ |
| L | _wchar_t_ |

#####String:

| Prefjo | Descripción | Ejemplo |
|--------|--------|-----|
| u8 | Literal codificado en UTF-8 |
| R | _raw strin_ | `R"(string with \backslash)"` |

#####Otros literales:

```cpp
bool foo = true;
bool bar = false;
int* p = nullptr;
```
