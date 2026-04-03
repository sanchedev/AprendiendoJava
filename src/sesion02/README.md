# Sesión 02

En esta sesión tocaremos el tema de las variables. Qué son y por qué usarlas.

Empezemos con un ejemplo.

Crea un archivo `Variables.java` e imprime en líneas separadas un saludo, en este caso `Hola`.

```java
public class Variables {
    public static void main(String[] args) {
        System.out.println("Hola");
        System.out.println("Hola");
        System.out.println("Hola");
    }
}
```

En consola verás

```
Hola
Hola
Hola
```

Pero ahora... ¿Qué pasa si queremos otro saludo? Podemos cambiarlo manualmente.

```java
// ...
        System.out.println("Saludo");
        System.out.println("Saludo");
        System.out.println("Saludo");
// ...
```

Ahora veríamos

```
Saludo
Saludo
Saludo
```

Pero es un poco costoso, ¿no?

Tener que cambiar manualmente todas las partes donde aparece para hacer lo que queremos.

Este es una de las razones para usar variables.

Ahora cambiemos el código a esto:

```java
// ...
        String saludo = "Saludo";
        
        System.out.println(saludo);
        System.out.println(saludo);
        System.out.println(saludo);
// ...
```

Verás que el resultado en consola es el mismo  pero algo cambio internamente.

Analizamos

En la primera línea estamos creando una `variable` con el nombre `saludo`.

Y en cada paréntesis de los `println`s está `saludo` sin las comillas.

## Variables

Una variable es una forma de almacenar valores para usarlos después. Puedes verlo como una caja 📦.

Está caja tiene una etiqueta para identificarla, este sería el nombre de la variable.

Está caja puede contener cosas dentro, lo que sería el valor que tiene.

Que pasa cuando creamos una variable llamada `saludo` con el valor de `"Saludo"`. Pues estamos tomando una caja, le ponemos la etiqueta `saludo` y dentro colocamos el texto `Saludo`.

Así que cuando usemos la palabra `saludo` sin las comillas en el código veremos el contenido que tiene dentro. Algo así como abrir la caja y revisar su interior.

Entonces al hacer

```java
System.out.println(saludo);
```

Java verá que hay dentro de `saludo`, al hacerlo encontrará `"Saludo"` así que imprimirá en consola

```
Saludo
```

Que pasa si ahora reemplazamos el valor de la variable en el código.

```java
// ...
        String saludo = "Hola";
        
        System.out.println(saludo);
        System.out.println(saludo);
        System.out.println(saludo);
// ...
```

Veremos

```
Hola
Hola
Hola
```

Porque cuando Java revisa el interior de saludo encontrará `"Hola"` haciendo que se imprima en consola eso.


## Creación de variables

Ahora te preguntarás, ¿Cómo creo una variable?

La respuesta es simple, tienes que seguir está estructura:

`[tipo de dato] [nombre de la variable] = [valor de la variable];`

Si vemos lo que teníamos antes podemos deducir que en: `String saludo = "Hola";`

- El tipo de dato es `String`
- El nombre es `saludo`
- El valor que tiene dentro es `"Hola"`

### Tipo de Dato

Al crear una variable le tienes que especificar que tipo de cosas puede tener dentro, como por ejemplo: textos (`String`), números (enteros `int`, decimales `double`), etc...

Es este caso el tipo es `String` por lo que estamos creando una variable que dentro puede contener un texto.

### Nombre

El nombre de una variable es importante, no puede contener espacios ni números al inicio por lo que `mi variable` y `1numero` son nombres inválidos. Además deben ser faciles de recordar y descriptivo para no cometer errores al usarlo.

Por ejemplo:

- `nombre`: Seguro contiene un `String`
- `edad`: Seguro contiene un `int`
- `altura`: Seguro contiene un `double`

### Valor

Después del nombre va un signo `=` y luego el valor. Este valor debe estar acorde al tipo de dato que le dijimos a la variable que puede contener.

Si una variable es un `String` entonces solo le podremos pasar textos entre comillas `""`.
Si es un `int` solo números enteros.
Y si es un `double` solo números decimales o terminados con `.0`.

Así que:

- `"Hola"`: Es un `String`
- `20`: Es un `int`
- `2.5`: Es un `double`

Siempre teniendo en cuenta que el tipo de dato y el valor deben estar relacionados.
Si haces:

```Java
String nombre = 20;
```

Java detectará un error y no será capaz de ejecutar tu programa porque `String` e `int` no están relacionados.

Por esto si hacemos:

```Java
double decimal = 2;
```

Si pasará pues `int` puede ser pasado como `double` fácilmente pero al revés **NO**.

```Java
int edad = 17.8;
```

Esto dará un error.

## Variables sin comillas

Cuando declaras una variable y luego la quieres usar, tienes que hacer referencia al nombre que le habías puesto.

Está referencia se hace sin comillas porque no es un `String` o texto sino una variable.

Veamos un ejemplo

```Java
String saludo = "Hola";

System.out.println(saludo);
System.out.println("saludo");
```

En consola se mostrará

```
Hola
saludo
```

**¿Se entiende el porqué?**

Al poner las comillas Java interpreta que lo que quieres hacer es poner un texto plano, por eso inprime `saludo` y no `Hola`.

## Reasignación

Vayamos usando otro tipo de dato.

Crea un archivo de **Java** llamado `Reasignando.java`.

Dentro del `main` pondremos lo siguiente:

```Java
int numero = 15;

System.out.println(numero);
```

Aquí solo creamos una variable y la mostramos en pantalla, por lo que veremos al ejecutar será:

```
15
```

Hasta ahora es algo que ya habíamos visto.

La **Reasignación** es cambiar el valor de una variable en tiempo de ejecución.

```Java
int numero = 15;

System.out.println(numero);

numero = 20;

System.out.println(numero);
```

Con este código ahora veremos:

```
15
20
```

Si te das cuenta en medio de los dos `println`s ejecutamos está línea:

```Java
numero = 20;
```

Cuando quieres reemplazar el valor que tiene una variable por otro valor se hace con esta estructura:

`[nombre de la variable] = [nuevo valor];`

Aquí el nombre de la variable es `numero` y el nuevo valor es `20`, como este nuevo valor cumple con ser un entero `int` como lo declaramos al crear la variable, la variable ahora tendrá dentro un valor diferente.

Entonces al hacer el segundo `println`, Java revisará el contenido de `numero` y al ver que su valor es `20` se lo dará el `println` y este lo mostrará en pantalla.

Es hora de los [ejercicios](./ejercicios/README.md).

Da lo mejor que puedas

## Uso de la palabra clave `var`

Cuando entiendas a usar bien las variables y puedas hacer los ejercicios propuestos correctamente sin problemas podrás entender está sección.

Puede que te hayas dado cuenta que es un poco redundante tener que poner indicar el tipo de dato manualmente, como cuando al incio de una variable pones `String` cuando el valor es un `String` o poner `int` cuando el valor es `10`. Para esto se creo `var`.

Al usar var la estructura de creación de una variable no cambia mucho:

`var [nombre] = [valor];`

Cuando usas `var` la variable obtendrá el tipo de valor del valor que le pases.

Por ejemplo, podríamos pasar de:

```Java
String saludo = "Hola";
```

a

```Java
var saludo = "Hola";
```

Realmente los dos son lo mismo, la única diferencia es que al primero el tipo de dato es explícito y en el segundo se infiere.

`"Hola"` es un `String` por lo que el tipo de dato de `saludo` será `String`.