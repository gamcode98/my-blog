---
sidebar_position: 2
---

# "Hola, Mundo" en Go

En este tutorial, aprenderemos a crear un programa "Hola, Mundo" en el lenguaje de programación Go. También entenderemos qué significan `package`, `func` y cómo usar el paquete `fmt` en Go.

## Paso 1: Instala Go

Asegúrate de tener Go instalado en tu sistema siguiendo las instrucciones en la [documentación oficial de Go](https://golang.org/doc/install).

## Paso 2: Crea un nuevo directorio

Abre tu terminal y crea un nuevo directorio para tu proyecto "Hola, Mundo" de Go. Puedes hacerlo con el siguiente comando:

```bash
mkdir holamundo-go
cd holamundo-go
```

## Paso 3: Crea un archivo Go

Dentro del directorio holamundo-go, crea un archivo Go con el nombre que prefieras. Por ejemplo, puedes usar "holamundo.go" para este tutorial:

```bash
touch holamundo.go
```

## Paso 4: Edita el archivo Go

Abre el archivo "holamundo.go" con tu editor de texto y agrega el siguiente código:

```go
package main

import "fmt"

func main() {
    fmt.Println("¡Hola, Mundo!")
}
```

`package main`: En Go, un programa siempre comienza con el paquete main. Define que este archivo es el punto de entrada de tu programa.

`import "fmt"`: Importamos el paquete fmt, que proporciona funciones para formatear texto y salida.

`func main()`: Esta es la función principal de tu programa. Es el punto de entrada, y todo programa Go debe tener una función main. Aquí es donde comienza la ejecución del programa.

`fmt.Println("¡Hola, Mundo!")`: Utilizamos la función Println del paquete fmt para imprimir "¡Hola, Mundo!" en la consola.

## Paso 5: Compila y ejecuta el programa

Guarda el archivo "holamundo.go" y, desde la terminal, dentro del directorio holamundo-go, compila y ejecuta el programa con el siguiente comando:

```bash
go run holamundo.go
```

Verás la salida en la consola que dice "¡Hola, Mundo!".

¡Felicidades! Acabas de crear y ejecutar tu primer programa "Hola, Mundo" en Go. Ahora sabes lo que significa package main, cómo definir una función main, y cómo usar el paquete fmt para imprimir en la consola.
