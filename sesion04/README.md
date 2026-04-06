# Sesión 04: Tu programa escucha

Hasta ahora, nosotros le dábamos los datos al programa directamente en el código. Hoy aprenderemos a hacer que el programa se detenga y espere a que el usuario escriba algo.

Para lograrlo, necesitamos una herramienta llamada Scanner.

## Moldes y Objetos (Instancias)

Antes de usar el `Scanner`, debemos entender cómo "crear" herramientas en Java.

Imagina que quieres hacer galletas de estrella. Necesitas un molde. El molde no es una galleta, es solo la idea o la forma. Para tener una galleta real, tienes que usar el molde sobre la masa.

 * La Clase (Molde): Es el plano o diseño. Ejemplo: `Scanner`.
 * El Objeto (Instancia): Es la herramienta real que ya puedes usar.
 * `new`: Es la palabra mágica que le dice a Java: "Usa el molde para crear un objeto real".

¿Cómo se escribe?

```java
Scanner miEscaner = new Scanner(System.in);
```

 * `Scanner`: El tipo de herramienta (el molde).
 * `miEscaner`: El nombre que tú le das a tu herramienta.
 * `new Scanner(...)`: Aquí estamos fabricando la herramienta real.
 * `System.in`: Es el "cable" que conecta el `Scanner` con tu teclado.

## Los Imports

Java es enorme y tiene miles de herramientas. Para que tu programa no sea pesado, Java no carga todas las herramientas al mismo tiempo.

Si quieres usar el `Scanner`, tienes que ir al "garaje" y traerlo. Esto se hace con un import al principio de todo tu archivo:

```java
import java.util.Scanner; // "Oye Java, trae el Scanner de la caja de Utilidades"

public class MiPrograma { 
    // ...
}
```

## Codeando

Vamos a crear un programa que te pregunte tu nombre y te salude.

Crea Leyendo.java y prepara la estructura básica con el import:

```java
import java.util.Scanner;

public class Leyendo {
    public static void main(String[] args) {
        // Creamos nuestra herramienta de lectura una sola vez
        Scanner lector = new Scanner(System.in);
        
        // El código sigue abajo...
    }
}
```

Ahora vamos a pedirle algo al usuario. Usaremos el método `.nextLine()` que sirve para leer texto.

```java
        System.out.print("¿Cómo te llamas? "); 
        
        // El programa se detendrá aquí hasta que presiones ENTER
        String nombre = lector.nextLine();
```

Ahora que el nombre está guardado en la variable nombre, ¡úsalo!

```java
        System.out.println("¡Mucho gusto, " + nombre + "!");
        
        // Buena práctica: cerrar la herramienta al terminar
        lector.close();
```

## Diferentes tipos de lectura

El Scanner tiene una herramienta para cada tipo de dato que aprendimos en la ***Sesión 02***:

| Lo que el usuario escribe | Método del Scanner | Ejemplo de uso |
|---|---|---|
| Texto | nextLine() | String t = lector.nextLine(); |
| Número entero | nextInt() | int n = lector.nextInt(); |
| Número decimal | nextDouble() | double d = lector.nextDouble(); |

¡Cuidado con el choque de tipos!

Si le dices a Java `int edad = lector.nextInt();` y el usuario escribe `"Diecisiete"` (en letras), el programa va a "explotar" (te dará un error rojo).

> Dato: El `Scanner NO controla los datos que el usuario pueda poner, por eso siempre asegúrate de que el método coincida con lo que esperas recibir. Así el programa se cortará si se pone un dato incorrecto.

**¿Sabes cuál es el siguiente paso?**

Resulve estos [ejercicios](./EJERCICIOS.md) para comenzar a probar.
