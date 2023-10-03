---
sidebar_position: 3
---

# Variables, Constantes y Zero Values en Go

En este tutorial, exploraremos los conceptos de variables, constantes y zero values en el lenguaje de programación Go.

## Variables en Go

### Declaración de Variables

En Go, puedes declarar una variable de la siguiente manera:

```go
var nombreVariable tipo
```

Por ejemplo:

```go
var numeroEntero int
```

## Inicialización de Variables

Puedes inicializar una variable al momento de declararla:

```go
var numeroEntero int = 42
```

O puedes dejar que Go infiera el tipo de dato automáticamente:

```go
nombreVariable := valor
```

Por ejemplo:

```go
nombre := "Juan"
edad := 30
```

## Zero Values en Go

En Go, todas las variables se inicializan con un valor zero según su tipo. Los zero values son:

`0` para tipos numéricos (integers y floats).

`false` para valores booleanos.

`""` (cadena vacía) para strings.

`nil` para punteros, slices, maps, interfaces y canales.

Por ejemplo, si declaras una variable sin asignarle un valor:

```go
var x int
var y string
var z bool
```

`x` será igual a `0`, `y` será una cadena vacía, y `z` será `false`.

## Constantes en Go

En Go, puedes declarar constantes utilizando la palabra clave `const`:

```go
const nombreConstante tipo = valor
```

Por ejemplo:

```go
const pi float64 = 3.14159265359
const nombre = "Juan"
```

Las constantes son valores que no pueden cambiar después de ser declarados y son útiles cuando necesitas valores inmutables en tu programa.
