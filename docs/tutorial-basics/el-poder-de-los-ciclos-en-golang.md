---
sidebar_position: 9
---

# Ciclos en Go (for, for como while y for infinito)

Los ciclos son una parte fundamental de la programación, y en Go, tenemos varias formas de implementarlos. En este tutorial, exploraremos cómo utilizar los ciclos `for`, `for` como `while`, y `for` infinito en Go, junto con algunos datos útiles, trucos y buenas prácticas.

## Ciclo `for` en Go

El ciclo `for` en Go se utiliza para ejecutar un bloque de código repetidamente mientras se cumple una condición. La forma más común es:

```go
for inicialización; condición; actualización {
    // Cuerpo del ciclo
}
```

- `inicialización`: Se ejecuta una vez al comienzo.

- `condición`: Se verifica antes de cada iteración.

- `actualización`: Se ejecuta después de cada iteración.

Ejemplo:

```go
for i := 0; i < 5; i++ {
  fmt.Println(i)
}
```

## Ciclo `for` como while en Go

En Go, puedes simular un ciclo while utilizando la siguiente sintaxis:

```go
for condición {
  // Cuerpo del ciclo
}
```

Este tipo de ciclo se ejecutará mientras la condición sea true. Por ejemplo:

```go
contador := 0
for contador < 5 {
  fmt.Println(contador)
  contador++
}
```

## Ciclo `for` infinito en Go

Si deseas crear un ciclo infinito en Go, puedes hacerlo de la siguiente manera:

```go
for {
  // Cuerpo del ciclo
}
```

Ten cuidado al usar ciclos infinitos y asegúrate de tener una forma de salir del ciclo, como una declaración `break` o una condición de salida.

## Uso de break y continue

- `break`: Se utiliza para salir inmediatamente de un ciclo.
- `continue`: Se utiliza para saltar a la siguiente iteración del ciclo.

```go
for i := 0; i < 10; i++ {
  if i == 5 {
    break // Sale del ciclo cuando i es igual a 5
  }
  if i%2 == 0 {
    continue // Salta a la siguiente iteración cuando i es par
  }
  fmt.Println(i)
}
```
