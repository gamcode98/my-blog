---
sidebar_position: 12
---

# Uso de `defer`, `break` y `continue` en Go

En este tutorial, exploraremos el uso de las palabras clave `defer`, `break` y `continue` en el lenguaje de programación Go. Estas palabras clave son herramientas poderosas para controlar el flujo de tu programa y garantizar la ejecución adecuada de ciertas tareas.

## `defer` en Go

La palabra clave `defer` se utiliza para programar una función para que se ejecute justo antes de que finalice la función actual. Esto es útil cuando necesitas limpiar recursos, como cerrar archivos o conexiones de red, al final de una función, independientemente de cómo se salga de ella.

Ejemplo:

```go
func leerArchivo() {
  archivo, err := os.Open("archivo.txt")
  if err != nil {
    // Manejo de errores
    return
  }
  defer archivo.Close() // Cierra el archivo al final de la función

  // Leer y procesar el archivo
}
```

En este ejemplo, el archivo se cerrará automáticamente cuando la función leerArchivo finalice, incluso si hay un error y se produce una salida temprana.

**Nota**: La buena practica nos dice que usemos un `defer` por función.

## `break` en Go

La palabra clave break se utiliza para salir de un bucle (for, switch, o select) antes de que termine su ciclo normal. Puedes utilizar break para detener un bucle cuando se cumple cierta condición.

Ejemplo con for:

```go
for i := 1; i <= 10; i++ {
  if i == 5 {
    break // Sale del bucle cuando i es igual a 5
  }
  fmt.Println(i)
}
```

## `continue` en Go

La palabra clave continue se utiliza para omitir la iteración actual de un bucle y pasar a la siguiente. Puedes utilizar continue para saltar una iteración cuando se cumple cierta condición sin salir del bucle por completo.

Ejemplo con for:

```go
for i := 1; i <= 5; i++ {
  if i == 3 {
    continue // Salta la iteración cuando i es igual a 3
  }
  fmt.Println(i)
}
```
