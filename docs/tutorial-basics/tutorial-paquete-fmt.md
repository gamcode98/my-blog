---
sidebar_position: 6
---

# Uso del Paquete `fmt` en Go

En este tutorial, exploraremos el paquete `fmt` en el lenguaje de programación Go. El paquete `fmt` se utiliza para realizar operaciones de entrada y salida formateadas en consola, lo que permite imprimir resultados y leer datos de usuario de una manera estructurada.

## Importación del Paquete `fmt`

Para utilizar el paquete `fmt`, debes importarlo en tu programa Go. Esto se hace de la siguiente manera:

```go
import "fmt"
```

Asegúrate de agregar esta línea al comienzo de tu archivo Go antes de utilizar las funciones del paquete `fmt`

## Imprimir en la Consola

El paquete `fmt` proporciona varias funciones para imprimir en la consola. La más común es `Println`, que se utiliza para imprimir una línea de texto en la consola, seguida de un salto de línea. Aquí tienes un ejemplo:

```go
package main

import "fmt"

func main() {
  fmt.Println("¡Hola, Mundo!")
}
```

Este programa imprimirá "¡Hola, Mundo!" en la consola y luego realizará un salto de línea.

## Formateo de Texto

El paquete `fmt` también permite formatear texto con la función `Printf`. Puedes utilizar marcadores de posición para insertar valores en el texto formateado. Aquí tienes un ejemplo:

```go
package main

import "fmt"

func main() {
  nombre := "Juan"
  edad := 30
  fmt.Printf("Hola, soy %s y tengo %d años.\n", nombre, edad)
}
```

En este ejemplo, `%s` se utiliza para formatear la cadena de texto `nombre`, y `%d` se utiliza para formatear el valor entero `edad`. La salida será "Hola, soy Juan y tengo 30 años."

`%s`: Este marcador de posición se utiliza para formatear cadenas de texto. Cuando se encuentra `%s` en una cadena de formato, se espera que un valor de tipo cadena de texto (`string`) lo reemplace.

`%d`: Este marcador de posición se utiliza para formatear valores enteros. Cuando se encuentra `%d` en una cadena de formato, se espera que un valor de tipo entero (`int`) lo reemplace.

## Marcadores de Posición Adicionales

demás de `%s` y `%d`, el paquete fmt en Go admite otros marcadores de posición útiles:

`%v`: Este marcador de posición se utiliza para formatear un valor en su representación predeterminada. Es útil cuando deseas imprimir valores de diferentes tipos.

```go
numero := 42
texto := "Hola"
fmt.Printf("Número: %v, Texto: %v\n", numero, texto)
```

`%T`: Este marcador de posición se utiliza para imprimir el tipo de un valor.

```go
numero := 42
fmt.Printf("El tipo de 'numero' es: %T\n", numero)
```

Estos marcadores de posición adicionales te permiten formatear datos de manera más flexible y obtener información sobre los tipos de valores que estás utilizando.

## Lectura de Datos de Usuario

Para leer datos de usuario desde la consola, puedes utilizar la función `Scan` del paquete `fmt`. Aquí tienes un ejemplo de cómo leer un número entero:

```go
package main

import "fmt"

func main() {
  var numero int
  fmt.Print("Ingrese un número: ")
  fmt.Scan(&numero)
  fmt.Printf("Usted ingresó: %d\n", numero)
}
```

Este programa solicitará al usuario que ingrese un número y luego imprimirá el número ingresado.
