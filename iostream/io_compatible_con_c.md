Entrada y salida compatible con C
====

No sólo pueden utilizarse los streams para obtener una interacción de entrada y salida con el usuario mediante los streams. **C++** usa recompatibilidad siendo capaz de usar la biblioteca `stdio` de **C**.

Es decir, para expresar:

```cpp
int a;
cin>>a;
```

Podemos utilizar `scanf` para leer una entrada formateada.

```cpp
int a;
scanf("%d", &a);
```

E imprimir por salida estandar:

```cpp
cout << "Tengo " << age << " años y mi codigo postal es " << codigo_postal;
```

Somos capaces de sustituirlo por la sentencia equivalente en `printf`:

```cpp
printf("Tengo %d y mi codigo postal es %d", edad, codigo_postal);
```

Como los tipos básicos son heredados de **C**, los formatos y los caracteres de escape para reconocer cada uno de ellos es similar. 

**Aviso**: El caso especial de los string nos puede causar errores debido a que su representación en ambos lenguajes no es la misma. Como sabemos en **C** un string en un array de caracteres terminado con el carácter de escape `\0`, en cambio en **C++** tiene una clase propia con operaciones y miembros especiales. Por suerte, existe una conversión sobre la clase string `.c_string()` que nos permite imprimirlos mediante el `printf`.

