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
