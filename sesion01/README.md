# Sesión 01: Hablando con la Computadora

En esta primera sesión aprenderemos a hacer que nuestro programa nos "hable". En programación, esto se conoce como **imprimir en consola**.

## ¿Qué es la Consola y por qué la usamos?

Imagina que la consola es como el chat entre tú y tu programa. Como aún no estamos creando ventanas con botones o colores, la consola es el único lugar donde podemos ver si nuestro código está funcionando correctamente.
Usamos la impresión para:

 * Ver resultados: "El resultado de la suma es 10".
 * Rastrear errores: "El programa llegó hasta este punto sin caerse".

## System.out.println

Para mostrar algo en pantalla en Java, usamos una frase larga. No te asustes, vamos a desarmarla como un juguete:

| Parte | ¿Qué significa? |
|-------|-----------------|
| System | Es el sistema de tu computadora. |
| .out | Significa "salida" (queremos sacar información hacia afuera). |
| .println | Es la acción de "imprimir una línea" (del inglés print line). |

> *Dato curioso*: Se dice `imprimir` porque hace muchos años las computadoras no tenían pantallas; el resultado salía literalmente en una hoja de papel.

## print vs println

Java te da dos opciones para mostrar texto.

La diferencia es sutil pero muy importante:

### System.out.print (Sin el "ln")

Imprime el texto y deja el cursor ahí mismo, en la misma línea. Si escribes otro comando abajo, se pegará al anterior.

```java
System.out.print("Hola");
System.out.print("Mundo");
```

Resultado:

```
HolaMundo
```

### System.out.println (Con el "ln")

Imprime el texto y luego hace un salto de línea (como presionar "Enter"). El siguiente mensaje aparecerá abajo.

```java
System.out.println("Hola");
System.out.println("Mundo");
```

Resultado:

```
   Hola
   Mundo 
```

## ¿Por qué hay tanto código extra al crear un archivo?

Cuando creas un archivo nuevo, verás que Java escribe varias líneas por ti. No intentes memorizar esto todavía, solo entiéndelo como una matrioshka 🪆 (una caja dentro de otra):

 * La Clase (lo que va después del `public class`): Es el nombre de tu archivo. Todo tu código debe vivir aquí dentro.
 * El Método Main (`public static void main`): Es la puerta de entrada. Cuando le das a "Play", Java busca esta línea exacta para empezar a leer. Si no está, el programa no arranca.

```java
public class HolaMundo { // 📦 Caja Grande (El archivo)
    public static void main(String[] args) { // 🚪 Puerta de entrada
        
        // Aquí va tu código (Lo que el programa hará)
        System.out.println("¡Lo logré!");
        
    } // 🚪 Cerramos la puerta
} // 📦 Cerramos la caja
```

***Para evitar errores:***

 * El punto y coma (;): Es como el punto final de una oración. Si lo olvidas, Java no sabrá dónde termina tu instrucción.
 * Las comillas (" "): Se usan para texto.
   * "1 + 1" mostrará literalmente `1 + 1`.
   * 1 + 1 (sin comillas) mostrará el resultado: `2`.
 * Mayúsculas: Java es muy estricto. No es lo mismo system que System. Fíjate bien en la S mayúscula.

## A practicar

No te quedes solo con la lectura. Ve a la carpeta de ejercicios y pon a prueba lo que aprendiste:

[Enlace a los ejercicios de la Sesión 01](./EJERCICIOS.md)
