---
sidebar_position: 5
---

# Tipos de Datos Primitivos en Go

En este tutorial, exploraremos los tipos de datos primitivos en el lenguaje de programación Go. Los tipos de datos primitivos son la base de cualquier programa y representan valores simples como números, caracteres y booleanos.

## Tipos de Datos Numéricos

Go admite varios tipos de datos numéricos que pueden representar números enteros o de punto flotante:

### Enteros (int)

Los enteros se utilizan para representar números enteros, ya sean positivos o negativos. Go proporciona diferentes tamaños de enteros, como `int`, `int8`, `int16`, `int32` y `int64`, dependiendo de la cantidad de bits que ocupan en memoria.

```go
var entero int = 42
```

### Punto Flotante (float)

Los números de punto flotante se utilizan para representar valores con decimales. Go proporciona dos tipos principales: `float32` y `float64`.

```go
var decimal float64 = 3.14159265359
```

## Tipos de Datos de Texto

Go utiliza el tipo `string` para representar cadenas de texto.

```go
var nombre string = "Juan"
```

## Tipos de Datos Booleanos

El tipo `bool` se utiliza para representar valores booleanos, es decir, `true` o `false`.

```go
var esMayorDeEdad bool = true
```

## Tipos de Datos Comunes

Además de los tipos de datos mencionados anteriormente, Go ofrece otros tipos de datos incorporados, como:

`byte`: Un alias para uint8.

`rune`: Un alias para int32, utilizado para representar caracteres Unicode.

`complex64` y `complex128`: Para números complejos.

## Conversión de Tipos

Puedes convertir entre diferentes tipos de datos en Go utilizando la sintaxis `TipoDato(valor)`

```go
var entero int = 42
var decimal float64 = float64(entero)
```
