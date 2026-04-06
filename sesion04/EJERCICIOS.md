# Sesión 04

## Concepto clave

- `Scanner` -> herramienta para leer datos del usuario
- `new` -> crear algo nuevo a partir de una clase
- `import` -> traer una utilidad al código
- `nextLine()` -> leer texto (String)
- `nextInt()` -> leer números enteros (int)

## Ejercicios

### 1. Primer input

Pide al usuario su nombre y muéstralo en consola.

Objetivo:

```
Ingresa tu nombre: [nombre]
Saludos [nombre]
```

:: Reemplaza `[nombre]` con lo que el usuario introduzca por consola.

### 2. Input + variable

Pide al usuario su color favorito y guárdalo en una variable.
Luego muestra:

```
¿Cuál es tu color favorito?: [color]
Te gusta el [color]
```

:: Reemplaza `[color]` por el valor ingresado.

### 3. Dos inputs

Pide al usuario su nombre y su edad.
Luego muestra:

```
Nombre: [nombre]
Edad: [edad]
Hola [nombre], tienes [edad] años
```

:: Reemplaza `[nombre]` y `[edad]` por los valores ingresados.

### 4. Usar print correctamente

Haz lo mismo que el ejercicio anterior pero ahora pide la información que quieras y muéstrala.

El resultado debe verse bien.

### 5. Número + operación

Pide al usuario un número entero.
Luego súmale 5 y muestra el resultado.

Ejemplo usando `10`:

```
Ingresa un número: 10
Resultado: 15
```

### 6. Dos números

Pide dos números enteros y muestra su suma.

Ejemplo usando `2` y `4`:

```
Número 1: 4
Número 2: 6
Resultado: 10
```

### 7. Mezcla de texto y número

Pide al usuario su nombre y un número.
Luego muestra:

```
Hola [nombre], tu número es [numero]
```

### 8. Detectar error

Este código tiene un problema:

```java
Scanner sc = new Scanner(System.in);
int numero = sc.nextLine();
```

Explica:

- ¿Cuál es el error?
- ¿Cómo lo solucionarías?

### 9. ¿Qué pasará?

Ejecuta este código:

```java
Scanner sc = new Scanner(System.in);

System.out.print("Nombre: ");
String nombre = sc.nextLine();

System.out.print("Edad: ");
int edad = sc.nextInt();

System.out.println(nombre + edad);
```

- Enseña que te da
- Teoriza el porqué crees que muestra eso

### 10. Desafío final

Crea un programa que pida:

- Tu nombre
- Tu edad
- Tu comida favorita

Y que después de pedir los datos muestre EXACTAMENTE esto:

```
Hola [nombre]
Tienes [edad] años
Tu comida favorita es [comida]
En 5 años tendrás [edad + 5]
```

:: Usa operaciones para calcular la nueva edad
:: Reemplaza los valores con lo ingresado por el usuario

---

## Reglas

- Respeta espacios y saltos de línea
- No copies y pegues sin entender
- Usa `Scanner` correctamente
- Declara variables cuando sea necesario

## Consejo

Si algo no funciona, imprime los valores para ver qué está pasando.

## Meta

- Entender cómo leer datos del usuario
- Saber cuándo usar `nextLine()` y `nextInt()`
- Poder combinar input con variables y operaciones
- Resolver mínimo 3 ejercicios
