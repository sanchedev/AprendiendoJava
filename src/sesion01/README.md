# Sesión 01

En esta sesión aprenderemos como "imprimir" en consola.

## ¿Por qué es importante esto?
Esto es muy relevante pues en muchos lenguajes de programación como **Java** la única manera de ver el paso a paso de tu código es por la consola. Por esto es importante que sepas cómo mostras cosas para que puedas **depurar**, **revisar** y **analizar** mejor tu código.

Ahora sí, ¿Cómo lo hago?

Pues en esta sesión te enseñaré dos formas y de las más usadas.

- `System.out.print`
- `System.out.println`

Ahora te parecerá raro.

Primero, está en inglés.

Segundo, tiene puntos.

Tercero, por qué se llama imprimir (print).

Y cuarto, por qué el segundo tiene un `ln` al final.

Aquí te cuento cada uno paso por paso.

## Inglés

La gran mayoría (por no decir todos) de lenguajes de programación están hechos para ser escritos y leídos en inglés, en estás sesiones escribiremos el código en una especie de Spanglish pero lo óptimo sería hacerlo completamente en inglés, no solo porque es un idioma mundial, sino también para no confundirnos al escribir.

## Los puntos entre palabras

Por el momento quédate con la idea de que esos puntos sirven para separar ideas de una misma operación.

Léelo así.

Si tenemos `System.out.println`.

Entonces podemos verlo como:

- `System`: Estamos accediendo al sistema
- `out`: Entramos a la salida (la consola)
- `println`: Imprimimos en una línea

Entonces la acción que queremos realizar es Imprimir en una línea en la consola del sistema.

## Imprimir

Antes de que existieran las pantallas y la consola, el resultado de una operación se imprimía a papel con una impresora conectada.

Los años pasaron pero esa aún sigue una memoria viva que quedó como referencia en muchos lenguajes de programación y habla común entre desarrolladores, si escuchas imprime x y hablamos entonces muy seguramente es para mostrar eso x en consola.

## Diferencia

Cuando quieres imprimir en la consola **Java** te das estás dos opciones, `print` y `println`.

Ese `ln` al final del segundo significa *en una línea*.

### Print

Cuando tú quieres imprimir mensajes con `print` vas a notar que los mensajes se pegan.

Este código:
```java
System.out.print("Hola");
System.out.print("Hola");
System.out.print("Hola");
```

Mostrará esto:
```
HolaHolaHola
```

Creo que puedes notar el problema... Usar `print` no hace un salto de línea al final por lo que el cursor se queda al final de una palabra cuando inicia la otra. Por eso se pegan.

Inténtalo por tu cuenta.

Crea un archivo Java Class y llámale `HolaMundo` y pega este código donde coincida:

```java
public clases HolaMundo {
    public static void main(String[] args) {
        System.out.print("Hola");
        System.out.print("Hola");
        System.out.print("Hola");
    }
}
```

Ejecutalo y verás que todo se pega.

Aquí es donde entra `println`.

### Println

Vuelve a tu archivo `HolaMundo.java` y pon al final de cada `print` un `ln` para que te quede así:

```java
public clases HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola");
        System.out.println("Hola");
        System.out.println("Hola");
    }
}
```

Ahora ejecútalo.

```
Hola
Hola
Hola
```

¿Notas el cambio?

Ahora inténtalo.

Resuelve los ejercicios que se encuentran en la carpeta `ejercicios` y resuelve los máximos que puedas.

## FAQ

**¿Cómo es la estructura?**

Cuando tú quieres imprimir algo en consola usas `print` o `println`.

Siempre de esta forma:

```java
System.out.print("[tu mensaje]");
```

:: Reemplaza `[tu mensaje]` con lo que quieras mostrar.

! No te olvides de las comillas dobles (`"`), esto le dice a **Java** que lo que tiene dentro es una cadena de texto y no código que puede ejecutar. No es lo mismo `"1 + 1"` que `1 + 1`.

El primero se mostraría como tal:

```
1 + 1
```

En cambio el segundo mostraría:

```
2
```
