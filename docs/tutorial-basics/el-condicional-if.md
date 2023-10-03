---
sidebar_position: 10
---

# Condicionales `if` en Go

En este tutorial, exploraremos el uso del condicional `if` en el lenguaje de programación Go. El condicional `if` es una estructura fundamental que te permite controlar el flujo de tu programa ejecutando diferentes bloques de código según una condición.

## Declaración de `if` en Go

En Go, la sintaxis básica del condicional `if` es la siguiente:

```go
if condición {
    // Código a ejecutar si la condición es verdadera
}
```

Por ejemplo, aquí hay un condicional if que verifica si un número es mayor que 10 y muestra un mensaje si la condición es verdadera:

```go
numero := 15
if numero > 10 {
    fmt.Println("El número es mayor que 10.")
}
```

## if...else en Go

Además del `if` simple, puedes utilizar un `else` para proporcionar un bloque de código que se ejecutará cuando la condición no sea verdadera:

```go
if condición {
  // Código a ejecutar si la condición es verdadera
} else {
  // Código a ejecutar si la condición es falsa
}
```

Ejemplo:

```go
numero := 5
if numero > 10 {
  fmt.Println("El número es mayor que 10.")
} else {
  fmt.Println("El número no es mayor que 10.")
}
```

## if...else if...else en Go

Puedes usar múltiples bloques else if para evaluar varias condiciones en orden. El primer bloque cuya condición sea verdadera tendrá su código ejecutado:

```go
if condición1 {
  // Código a ejecutar si la condición1 es verdadera
} else if condición2 {
  // Código a ejecutar si la condición2 es verdadera
} else {
  // Código a ejecutar si ninguna de las condiciones anteriores es verdadera
}
```

Ejemplo:

```go
numero := 7
if numero < 5 {
  fmt.Println("El número es menor que 5.")
} else if numero < 10 {
  fmt.Println("El número es menor que 10 pero mayor o igual a 5.")
} else {
  fmt.Println("El número es igual o mayor que 10.")
}
```

## if con Inicialización de Variables

En Go, puedes inicializar una variable antes de la evaluación de una condición en un condicional `if`. La variable estará disponible solo en el ámbito del condicional y cualquier bloque `else` o `else if` asociado.

```go
if variable := valorInicial; condición {
  // Código a ejecutar si la condición es verdadera
}
```

Ejemplo:

```go
if edad := 25; edad >= 18 {
  fmt.Println("Eres mayor de edad.")
} else {
  fmt.Println("Eres menor de edad.")
}
```
