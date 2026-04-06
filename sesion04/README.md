# Sesión 04

En este texto aprenderemos a usar el `Scanner`, una **utilidad** de Java para, literalmente, escanear la consola para recibir el `input` (entrada) del usuario.

## Instancias

Antes de enseñar como usarlo quiero resaltar algunas cosas antes.

Recuerdas que usamos la analogía de una caja para referirnos a las variables. Antes dentro poníamos cosas simples como por ejemplo, números. Pero ahora... ¿Qué pasa si queremos cosas más complejas? Volvamos a las analogías.

Digamos que queremos usar un martillo que no tenemos, pues lo compramos y para poder comprarlo tuvo que ser **creado**.

Una `clase` es como un _molde_, y cuando usamos `new` estamos creando una versión real de ese _molde_ que sí podemos usar.

A estas versiones reales se le llaman `instancias` y al proceso `instanciar`.

**Aclaración**: La clase `Martillo` no existe en Java, esto es con fines educativos pare el ejemplo.

Sigamos con lo del ejemplo del martillo. Para crear un _martillo_ en código a base de este _molde_ se haría así:

```Java
Martillo miMartillo = new Martillo();
```

Leámoslo un poco...

Esto tiene la estructura de una variable de `[tipo] [nombre] = [valor];`. Si reemplazamos:

- `[tipo]`: `Martillo`
- `[nombre]`: `miMartillo`
- `[valor]`: `new Martillo()`

Aquí vemos que el tipo empieza con una mayúscula, esto significa que proviene de una clase; es decir, que esta varible solo puede contener cosas salidas de este _molde_ llamado `Martillo`.

Sigamos con lo de `new Martillo()`.

La estructura:

```Java
new Martillo()
```

Viene de:

```
new [clase](parámetros)
```

Donde en nuestro caso:

- `[clase]`: `Martillo`
- `...parámetros`: Aquí no pusimos nada porque para crear un martillo no necesitamos nada. Esto viene de la sesión pasada, donde lo que poníamos dentro de los paréntesis se llamaban parámetros y se separaban por una coma.

_Y sí..._ `String` es una clase, solo que en lugar de hacer `new String("Hola")`, Java te permite recortarlo a `"Hola"` por comodidad.

Ahora que entiendes un poco esto vayamos a lo que te importa.

## Clase Scanner

Cuando tu quieres obtener la herramienta `Scanner`, al igual que con el ejemplo de `Martillo` tenemos que usar el _molde_.

```java
Scanner miEscaner = new Scanner(System.in);
```

Veamos esto con la estructura de instanciar:

- `[clase]`: `Scanner`
- `parámetros`: Nuestro único parámetro es `System.in`

Es decir, estamos obteniendo un `Scanner` a partir de su _molde_, el único parámetro que pide debe ser un objeto lector, o sea un `System.in`.

Como lo vimos en la sesión pasada, las _instancias_ de `String` tienen varios métodos, ya sabes, el `toUpperCase()`, `toLowerCase()`, esos.

### Métodos

Aquí es lo mismo con el `Scanner`.

Tenemos algunos métodos y te comentaré sobre algunos de ellos:

- `nextLine()`: Pausa tu programa hasta que el usuario escribe algo. Esta función devuelve un `String`.
- `nextInt()`: Hace lo mismo que `nextLine()`, solo que transforma todo ese texto en un entero, devolviendo un `int`.
- `close()`: Esta función **cierra** el `Scanner` haciendo que todos los métodos queden inutilizables.

Vamos a empezar con el código.

## Ejemplo con código

Creemos un archivo llamada `Leyendo.java`.

```java
public class Leyendo {
    public static void main(String[] args) {
        Scanner miEscaner = new Scanner(System.in);
    }
}
```

Te darás cuenta que tu código parece tener un error. Es raro, ¿no?.

Pues algo que no te dije son las importaciones.

### Importar

Imagina que estás haciendo una tarea que consiste en leer un libro, aquí no necesitar una **calculadora**. Pero si haces una tarea de matemática, sí.

En programación se le llama `importar` a traer una funcionalidad específica a tu proyecto, como la **calculadora**, a veces la necesitas y otras veces no.

Usualmente no usarías el `Scanner`; por esto, aunque Java tenga al `Scanner` al igual que tu una calculadora, nosotros le tenemos que decir que lo queremos usar, al igual que tu para cosas que tengan que ver con cálculo la tienes que usar.

Pero, ¿Cómo le decimos a Java que si lo queremos en nuestro código?, pues se hace de esta forma:

```java
import java.util.Scanner;
```

En español, Importar de Utilidades de Java el Escaner.

Esta línea la ponemos arriba del código. Así.

```java
import java.util.Scanner;

public class Leyendo {
    public static void main(String[] args) {
        Scanner miEscaner = new Scanner(System.in);
    }
}
```

Ya no te debería dar el error.

Ahora usemos nuestro _nuevo_ `Scanner`.

### Usando el Scanner

```java
import java.util.Scanner;

public class Leyendo {
    public static void main(String[] args) {
        Scanner miEscaner = new Scanner(System.in);

        miEscaner.nextLine();
    }
}
```

Si ejecutas este código verás que el programa se quedará congelado, o al menos eso parece. Si escribes teniendo en foco la consola verás que puedes. Si le das al `Enter` el programa terminará y se cerrará. Esto cumple con lo que digimos arriba. Este método `nextLine()` pausa el programa hasta que pongamos texto, luego lo continúa. Por ahora parece que no pasa nada porque no hacemos nada con los datos que nos llegan.

Hagamos algo más entretenido:

```java
import java.util.Scanner;

public class Leyendo {
    public static void main(String[] args) {
        Scanner miEscaner = new Scanner(System.in);

        System.out.print("Escribe tu nombre: ");
        String nombre = miEscaner.nextLine();
    }
}
```

Aquí las cosas conectan.

Primero, usamos `print` para escribir en consola

```
Escribe tu nombre:
```

Esto ya lo habíamos visto, usamos `print` y no `println` porque deja el cursor justo al final de la línea, entonces si escribo Juan pasa esto:

```
Escribe tu nombre: Juan
```

Interesante, ¿verdad?

Por ahora guardamos lo que el usuario nos da en una varible llamada `nombre` de tipo `String` porque como dijimos `nextLine()` devuelve un `String`, pero aún no hacemos nada con ella.

```java
import java.util.Scanner;

public class Leyendo {
    public static void main(String[] args) {
        Scanner miEscaner = new Scanner(System.in);

        System.out.print("Escribe tu nombre: ");
        String nombre = miEscaner.nextLine();

        System.out.print("Hola ");
        System.out.println(nombre);
    }
}
```

Ejecuta el código y ve la mágia.

Ahora sí usamos lo que el usuario nos da para saludarlo volviendo a usar `print`.

Si volvemos a escribir "Juan" pasará esto:

```
Escribe tu nombre: Juan
Hola Juan
```

Al final usamos el `println` para que no aparezca el texto de `BUILD SUCCESSFUL` pegado al nombre.

Ya tienes un código simple que hace mucho.

Ahora tus programas no solo podrán mostras cosas, sino que también podrán reaccionar a quien los usa.

**¿Sabes cuál es el siguiente paso?**

Resulve estos [ejercicios](./EJERCICIOS.md) para comenzar a probar.
