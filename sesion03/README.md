# Sesión 03: Máquinas y Resultados

Hasta ahora, hemos usado comandos como si fueran hechizos mágicos. Hoy entenderemos qué son realmente: máquinas que procesan información.

## ¿Qué es una Función?

Imagina una licuadora. Tú le introduces fruta (**entrada**), ella hace un proceso interno, y te entrega un jugo (**salida**).

En Java, los paréntesis `()` son la entrada de la máquina. Si están vacíos, es una máquina que no necesita nada para arrancar. Si tienen algo dentro, ese es su "ingrediente" o `parámetro`.

## El Retorno

Hay dos tipos de máquinas en la programación:

 * Las que solo hacen una acción: Como `System.out.println`. Le das un texto, lo muestra en consola y listo. **No te "devuelve" nada que puedas guardar.**
 * Las que te entregan un resultado: Como una calculadora. Le das `2 + 2` y te entrega un `4`. Ese `4` lo puedes guardar en una variable para usarlo después.


## Aclaraciones

### Comentarios

Corto está sección para hablar sobre los `comentarios`. Estos son partes del código que no se leen ni se ejecutan.

Imagina que tienes que hacer un informe a mano. Los comentarios serían simples Post-Its que pegarías encima y al entregarlo los sacas sin problemas.

Así que cada que veas un `//` significa que toda esa línea representa un `comentario`.

### Concatenación

Si ves a un `String` seguido de un símbolo más (`+`), significa que se va a concatenar.

Básicamente, concatenar es unir un texto con algo más.

```java
System.out.println("Hola " + "mundo");
```

Mostrará:

```
Hola mundo
```

## Jugando con el texto

Crea un archivo llamado `PruebaFunciones.java` y vamos a probar funciones que transforman texto.

A estas funciones que "viven" dentro de un objeto (como un `String`) las llamamos Métodos.

```java
public class PruebaFunciones {
    public static void main(String[] args) {
        String nombre = "java es genial";

        // 1. Usamos el método .toUpperCase()
        // Esta máquina recibe el texto y te DEVUELVE el mismo texto en mayúsculas.
        String nombreMayus = nombre.toUpperCase();

        System.out.println("Original: " + nombre);
        System.out.println("En mayúsculas: " + nombreMayus);
    }
}
```

**Pruébalo.**

Fíjate que usamos un punto `.` para entrar a las herramientas de nombre.

 * nombre.toUpperCase() -> "Dame lo que hay en nombre pero en grande".
 * nombre.toLowerCase() -> "Dame lo que hay en nombre pero en pequeño".


## Matemática (Math)

Java ya tiene una "caja de herramientas" llena de funciones matemáticas llamada `Math`.

Vamos a usar una para potencias:

```java
Math.pow(base, exponente).
```


Añade esto a tu código:

```java
// Queremos calcular 2 elevado al cubo (2^3)
double resultado = Math.pow(2, 3);

System.out.println("2 elevado a 3 es: " + resultado);
```

Analicemos:
 * Math.pow necesita dos ingredientes (parámetros), separados por una coma.
 * Nos devuelve un `double` (número decimal), por eso lo guardamos en una variable de ese tipo.


## De textos a números

A veces recibimos números pero "disfrazados" de texto (por ejemplo, cuando un usuario escribe en un formulario).

Si intentas sumar `"10" + 5`, Java hará un desastre y pegará los textos: `105`.

Para eso usamos `Integer.parseInt()`:

```java
String textoNumero = "10";
int numeroReal = Integer.parseInt(textoNumero); // Convierte "10" en el número 10

System.out.println(numeroReal + 5); // Ahora sí saldrá 15
```

## ¿Cómo leer un método?

Cuando veas algo como `saludo.toUpperCase()`, léelo así de derecha a izquierda:

 * `()` : Es una acción (ejecútala).
 * `toUpperCase` : La acción es "convertir a mayúsculas".
 * `.` : Pertenece a...
 * `saludo` : El objeto o variable que tiene la información.

> Nota: Ten cuidado con el vacío. Si intentas guardar el resultado de una función que no devuelve nada (como `println`), Java se fallará. Esto porque println es como un camión de basura: se lleva el mensaje, lo deja en la consola y se va. No te deja nada en la mano para guardar.

Ahora sí estás listo para los [Ejercicios de la Sesión 03](./EJERCICIOS.md).
