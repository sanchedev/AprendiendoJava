# Sesión 05: Camino dividido 

Hasta ahora, tus programas han sido como una línea recta. Hoy aprenderemos a crear bifurcaciones. Dependiendo de una condición, el programa elegirá el Camino A o el Camino B.

## El tipo de dato: boolean

Un booleano es el tipo de dato más simple que existe. Solo puede tener dos valores:

 * true (Verdadero / Encendido / Sí)
 * false (Falso / Apagado / No)

Es como un interruptor de luz: no hay puntos medios.

## Operadores de Comparación

Para obtener un booleano, solemos hacer "preguntas" matemáticas. Java nos responde con true o false.

| Operador | Significado | Ejemplo | Resultado |
|---|---|---|---|
| == | Igual a | 5 == 5 | true |
| != | Diferente de | 5 != 3 | true |
| > | Mayor que | 10 > 20 | false |
| < | Menor que | 8 < 15 | true |
| >= | Mayor o igual | 5 >= 5 | true |
| <= | Menor o igual | 4 <= 2 | false |

> Nota: No confundas = con ==.
>  * = sirve para guardar algo en una caja (asignar).
>  * == sirve para comparar si dos cosas son iguales.

## Operadores Lógicos

¿Qué pasa si quieres preguntar dos cosas al mismo tiempo? Usamos conectores:

 * AND (`&&`): Solo es verdad si TODO es verdad. (Ejemplo: Para entrar al cine necesitas entrada Y dinero para canchita).
 * OR (`||`): Es verdad si AL MENOS UNO es verdad. (Ejemplo: Entras a la fiesta si tienes invitación O si eres el cumpleañero).
 * NOT (`!`): Invierte el valor. Lo que es `true` se vuelve `false`.

## Estructuras de Control: if y else

### El if (Si condicional)

Es como un guardia de seguridad. Si cumples la regla, te deja pasar al bloque de código.

```
int edad = 17;

if (edad >= 18) {
    System.out.println("Eres mayor de edad");
}
```

Si ejecutas esto con `17`, no pasará nada. El código dentro de las llaves { } simplemente se **ignora**.

### El else (De lo contrario)

Aquí es donde corregimos el código. El else no lleva condición, porque es lo que ocurre automáticamente cuando el `if` falla.

```
int edad = 17;

if (edad >= 18) {
    System.out.println("Eres mayor de edad");
} else {
    // No necesitas poner (edad < 18), Java ya sabe que si no es mayor, es menor.
    System.out.println("Eres menor de edad");
}
```

## Codeando

Crea un archivo llamado `Acceso.java` y prueba este código. Vamos a mezclar lo que aprendimos de `Scanner` con `if-else`:

```java
import java.util.Scanner;

public class Acceso {
    public static void main(String[] args) {
        Scanner lector = new Scanner(System.in);

        System.out.print("Ingresa tu edad: ");
        int edad = lector.nextInt();

        System.out.print("¿Tienes carnet? (true/false): ");
        boolean tieneCarnet = lector.nextBoolean();

        // Usamos AND (&&) porque se deben cumplir AMBAS
        if (edad >= 18 && tieneCarnet == true) {
            System.out.println("¡Pasa a la universidad!");
        } else {
            System.out.println("Lo siento no puede pasar.");
        }
        
        lector.close();
    }
}

Analicemos el flujo:

 * Si tienes `20` años y pones `true`, la condición es `true && true` -> Entras.
 * Si tienes `20` años pero pones `false`, la condición es `true && false` -> No entras.
 * Si tienes `15` años, no importa si tienes entrada, el `if` fallará -> No entras.

Resumen:

 * `if`: El bloque que se ejecuta si la condición es verdadera.
 * `else`: El bloque "plan B" que se ejecuta si la condición es falsa.
 * Bloques `{ }`: Siempre asegúrate de abrir y cerrar las llaves para que Java sepa dónde termina tu decisión.

¡Hora de los desafíos!
Ahora que sabes cómo hacer que tu programa tome decisiones, ve a los [Ejercicios de la Sesión 05](./EJERCICIOS.md) y resuelve algunos.
