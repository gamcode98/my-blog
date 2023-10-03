---
sidebar_position: 11
---

# Condiciones Anidadas con `switch` en Go

En este tutorial, exploraremos cómo utilizar múltiples condiciones anidadas con la instrucción `switch` en el lenguaje de programación Go. La declaración `switch` es una forma eficiente y legible de manejar múltiples casos en función del valor de una expresión.

## Sintaxis Básica de `switch`

La sintaxis básica de `switch` en Go es la siguiente:

```go
switch expresion {
case valor1:
  // Código a ejecutar si expresion es igual a valor1
case valor2:
  // Código a ejecutar si expresion es igual a valor2
default:
  // Código a ejecutar si ninguna de las condiciones anteriores se cumple
}
```

Aquí tienes un ejemplo simple de switch en Go:

```go
dia := "lunes"
switch dia {
case "lunes":
  fmt.Println("Es el primer día de la semana.")
case "martes":
  fmt.Println("Es el segundo día de la semana.")
default:
  fmt.Println("Es un día de la semana desconocido.")
}
```

## Utilizando fallthrough

En Go, la ejecución normalmente no se propaga automáticamente a través de los casos en una declaración switch. Sin embargo, puedes usar la palabra clave fallthrough para lograr este comportamiento. Esto significa que si un caso con fallthrough se cumple, se ejecutará el siguiente caso sin importar su condición.

```go
switch numero {
case 1:
  fmt.Println("El número es 1.")
  fallthrough // Ejecutará el siguiente caso
case 2:
  fmt.Println("El número es 2.")
default:
  fmt.Println("Este caso se ejecutará debido a fallthrough.")
}
```

## switch con Tipos

Además de usar switch con valores, también puedes usarlo para evaluar el tipo de una variable. Esto es útil cuando deseas realizar acciones específicas en función del tipo de datos.

```go
var x interface{}
x = 42

switch x.(type) {
case int:
  fmt.Println("x es un entero.")
case string:
  fmt.Println("x es una cadena de texto.")
default:
  fmt.Println("x es de un tipo desconocido.")
}
```

## Múltiples Condiciones Anidadas

Puedes utilizar múltiples condiciones anidadas en una declaración `switch` para manejar diferentes casos en función de la expresión. Esto se hace al omitir la expresión en el `switch` y luego evaluar cada caso individualmente:

```go
numero := 5
switch {
case numero < 5:
  fmt.Println("El número es menor que 5.")
case numero == 5:
  fmt.Println("El número es igual a 5.")
case numero > 5:
  fmt.Println("El número es mayor que 5.")
default:
  fmt.Println("Este caso se ejecutará si ninguno de los anteriores es verdadero.")
}
```
