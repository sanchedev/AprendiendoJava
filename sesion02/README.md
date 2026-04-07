# Sesión 02: Guardando información

En la sesión anterior hicimos que la computadora hablara. Hoy vamos a darle memoria.

## Problemas

Abre tu editor de código, crea un archivo llamado Variables.java y escribe lo siguiente:

```java
public class Variables {
    public static void main(String[] args) {
        System.out.println("Hola, soy un mensaje");
        System.out.println("Hola, soy un mensaje");
        System.out.println("Hola, soy un mensaje");
    }
}
```

**Ejecútalo.**

Verás algo así: 

```
Hola, soy un mensaje
Hola, soy un mensaje
Hola, soy un mensaje
```

Es el mensaje repetido tres veces.

Ahora imagina que tu jefe te dice: "Ya no quiero que diga 'Hola', ahora quiero que diga 'Bienvenido'".

Tendrías que cambiarlo 3 veces.

Si tuvieras 1,000 líneas, estarías en problemas. Aquí es donde entran las variables.

## Tu primera Variable

Vamos a modificar tu código.

Borra lo que está dentro del main y cámbialo por esto:

```java
public class Variables {
    public static void main(String[] args) {
        String saludo = "Hola, soy una variable";

        System.out.println(saludo);
        System.out.println(saludo);
        System.out.println(saludo);
    }
}
```

**Pruébalo.**

El resultado es el mismo, pero mira la magia.

Cambia el texto "Hola, soy una variable" por "Soy un texto" solo en la primera línea.

**Ejecútalo de nuevo.**

¡Se actualizó en los tres println automáticamente!

Solo tuviste que cambiarlo en un lugar.

## ¿Qué es una Variable?

Imagina que una variable es una caja etiquetada.

- El Tipo: Es el tamaño/forma de la caja (¿Es para zapatos? ¿Es para libros?).
- El Nombre: Es la etiqueta que pegas por fuera para saber qué hay dentro sin abrirla.
- El Valor: Es el objeto que guardas dentro de la caja.

## ¿Cómo crear una variable?

En Java, para crear una caja debemos seguir este orden estricto:

```
TipoDeDato nombre = valor;
```

## Experimentando con Números

No todo en la vida es texto.

Java necesita saber qué tipo de datos estás guardando.

Añade estas líneas debajo de tus mensajes de saludo:

```java
int edad = 17;
double estatura = 1.75;

System.out.println(edad);
System.out.println(estatura);
```

Analicemos lo que acabas de escribir:

 * int: Es para números enteros (sin decimales).
 * double: Es para números con punto decimal.
 * String: Es para textos (siempre van entre comillas " ").

## Reglas para los Nombres

No puedes llamar a tus variables como sea. Java tiene reglas:

- No empezar con números:
  - 1puesto (ERROR)
  - puesto1 (correcto)
- Sin espacios:
  - mi edad (ERROR)
  - miEdad (correcto)
- Sensible a mayúsculas:
  - nombre y Nombre son dos cajas distintas.

### EL estilo CamelCase

En Java, si el nombre tiene varias palabras, la primera va en minúscula y las siguientes empiezan con Mayúscula.

Ejemplos:

- nombreDelUsuario (nombre del usuario)
- miEdad (mi edad)

## Errores

Para entender a Java, hay que romperlo.

Intenta hacer estos cambios en tu archivo y mira qué pasa en la consola:

 * El error de tipo: Cambia `int edad = 17;` por `int edad = "Diecisiete";`.
   * ¿Qué dice el error? Java te dirá que no puede meter un texto en una caja de números.
 * El error de las comillas: Intenta escribir `System.out.println(edad);` pero ponle comillas: `System.out.println("edad");`.
   * ¿Qué pasó? Ya no muestra el número `17`, sino la palabra literal `edad`.

> [!NOTE]
> Sin comillas buscas la caja por su etiqueta. Con comillas hablas directamente del texto.

## Reasignación

Una variable se llama así porque su valor puede variar.

Mira este ejemplo y agrégalo a tu código:

```java
int puntos = 10;
System.out.print("Puntos: ");
System.out.println(puntos);

puntos = 20; // Sacamos el 10 y metemos el 20
System.out.print("Puntos actualizados: ");
System.out.println(puntos);
```

> [!NOTE]
> Fíjate que la segunda vez no escribimos `int`. La caja ya está creada, solo le estamos cambiando lo que tiene dentro.


## Reto de salida

Antes de ir a los ejercicios, intenta crear una variable `double` para el precio de una galleta y una variable `String` para el nombre de la galleta.

**Imprime ambas en la consola.**

Si lograste que se vea en pantalla, estás listo para lo que viene.

¡Ahora sí, a los [EJERCICIOS](./EJERCICIOS.md)!
