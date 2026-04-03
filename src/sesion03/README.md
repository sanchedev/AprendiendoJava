# Sesión 03

En esta sesión aprenderemos a usar funciones ya existentes y entender qué significa que una función devuelva un valor.

## Funciones

Puede que te hayas preguntado, ¿Por qué cuando uso `System.out.println` tengo que poner esos paréntesis al final `()`?

Imagina un máquina.

La función que tendrá la máquina será la de sumar dos números, por lo que por arriba le tendrás que dar dos números y por abajo te dará un número que será el resultado.

Esto es una `función`.

Cuando quieres ejecutar esta máquina o como se le dice acá, *llamar a la función* tienes que poner estos paréntesis `()` al final.

Hay funciones que pedirán información externa, a esto le llamamos *parámetros*. Esto podemos decir que son las cosas que le damos a la máquina.

```Java
System.out.println("Hola");
```

Aquí podemos decir que estamos ejecutando la función `System.out.println` con el parámetro `"Hola"`. Y ¿qué hace `println` con lo que le damos? Lo muestra en la consola.

```
Hola
```

## Funciones que devuelven

Hay dos tipos de funciones, las que devuelven datos y las que no.

Por ejemplo, el `System.out.println` es una función que no devuelve datos.

Veamos algunas funciones que si retornan cosas.

Crea un archivo Java `Funciones.java`

```java
public class Funciones {
    public static void main(String[] args) {
        var saludo = "Buenas tardes";

        System.out.println(saludo.toUpperCase());
    }
}
```

Si ejecutamos esto veremos:
```
BUENAS TARDES
```

**¿Qué está pasando aquí?**

Ya deberías saber que `saludo` contiene `"Buenas tardes"` que es un `String`.

La función `saludo.toUpperCase()` es una función que devuelve el `String` en mayúsculas, si `saludo` era `"Buenas tardes"`, ahora será `"BUENAS TARDES"`.

Ahora al resultado de esta función lo estamos pasando como *parámetro* a `System.out.println` para verlo por consola.

Lo mismo podemos hacer con `saludo.toLowerCase()`. La cual devolverá `buenas tardes`.

Si te das cuenta `saludo` y `toUpperCase` están unidos por un punto. Este punto es una forma de acceder dentro de.

Al hacer `saludo.toUpperCase` estamos accediendo a `toUpperCase` que está dentro de `saludo`. A estos se le llaman `métodos`, funciones que están dentro de otros objetos. A los `métodos` los puedes entender como acciones que puedes realizar con el objeto. 

Por ejemplo `toUpperCase()` transforma el `String` en mayúsculas.

`println` muestra mensajes en `System.out` (Salida del sistema) insertando un salto de línea al final.

Incluso podemos guardar los datos que nos devuelvan las funciones para usarlas después.

```java
var saludo = "Buenas tardes";
var saludoMay = saludo.toUpperCase();

System.out.println(saludoMay);
```

Inclusive así queda más entendible.

:: Aclaración: `saludo.toUpperCase()` es un `String` por eso cuando usamos `var` Java detecta la variable como `String`.

```java
var saludo = "Buenas tardes";

var saludoMay = saludo.toUpperCase();
System.out.println(saludoMay);

var saludoMin = saludo.toLowerCase();
System.out.println(saludoMin);
```

Evidentemente no solo existen estás funciones. Existen miles más. Veamos unas cuantas.

### double Math.pow(double base, double exponente)

```java
double num = Math.pow(2, 3);
System.out.println(num);
```

Si ejecutas esto verás que en consola sale `8`. `Math.pow` es una función que espera dos parámetros, `double base` y `double exponente`. Está devolverá a la `base` elevada al `exponente`.

Aquí la `base` es `2` y el `exponente` es `3`. `2³` es igual a `8`, por lo que devuelve `8`.

Hay que tener en cuenta que esta función devuelve el número como `double`, así que si quieres usarlo como un entero descartando los decimales necesitaras realizar un proceso extra antes.

### int Integer.parseInt(String numero)

Esta función recibe un parámetro del tipo `String` y devolverá un número `int`.

```java
var num = Integer.parseInt("10");

System.out.println(num + 5);
```

Aquí le sumo `5` para demostrar que sí devolvió un número.

```
15
```

Ahora ya estás listo para empezar con los [ejercicios](./ejercicios/README.md).