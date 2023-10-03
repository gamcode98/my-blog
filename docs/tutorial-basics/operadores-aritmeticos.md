---
sidebar_position: 4
---

# Operadores Aritméticos en Go

En este tutorial, exploraremos los operadores aritméticos en el lenguaje de programación Go. Los operadores aritméticos te permiten realizar cálculos matemáticos en tus programas Go.

## Operadores Aritméticos Básicos

### Suma (+)

El operador `+` se utiliza para sumar dos valores.

Ejemplo en Go:

```go
a := 5
b := 3
resultado := a + b
fmt.Println(resultado) // Imprimirá 8
```

### Resta (-)

El operador `-` se utiliza para restar el segundo valor del primero.

Ejemplo en Go:

```go
a := 10
b := 4
resultado := a - b
fmt.Println(resultado) // Imprimirá 6
```

### Multiplicación (*)

El operador `*` se utiliza para multiplicar dos valores.

Ejemplo en Go:

```go
a := 7
b := 8
resultado := a * b
fmt.Println(resultado) // Imprimirá 56
```

### División (/)

El operador `/` se utiliza para dividir el primer valor por el segundo.

Ejemplo en Go:

```go
a := 20
b := 5
resultado := a / b
fmt.Println(resultado) // Imprimirá 4
```

### Módulo (%)

El operador `%` se utiliza para obtener el resto de la división del primer valor por el segundo.

Ejemplo en Go:

```go
a := 17
b := 5
resultado := a % b
fmt.Println(resultado) // Imprimirá 2
```

## Operadores de Incremento y Decremento

### Incremento (++) y Decremento (--)

Go admite los operadores de incremento (++) y decremento (--) para aumentar o disminuir el valor de una variable en uno.

Ejemplo en Go:

```go
a := 5
a++
fmt.Println(a) // Imprimirá 6

b := 10
b--
fmt.Println(b) // Imprimirá 9
```
