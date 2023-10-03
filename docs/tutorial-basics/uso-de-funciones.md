---
sidebar_position: 7
---

# Uso de Funciones y Funciones Anónimas en Go

En este tutorial, exploraremos el uso de funciones y funciones anónimas en el lenguaje de programación Go. Las funciones son bloques de código reutilizables que realizan tareas específicas, y las funciones anónimas son funciones sin un nombre definido que se pueden utilizar de manera flexible.

## Declaración de Funciones en Go

En Go, las funciones se declaran de la siguiente manera:

```go
func nombreFuncion(parametro1 tipo, parametro2 tipo) tipoDeRetorno {
  // Cuerpo de la función
  // ...
  return valorDeRetorno
}
```

Por ejemplo:

```go
func suma(a int, b int) int {
  resultado := a + b
  return resultado
}
```

## Llamada a Funciones en Go

Puedes llamar a una función en Go utilizando su nombre y proporcionando los argumentos necesarios. Aquí tienes un ejemplo de cómo llamar a la función suma:

```go
resultado := suma(5, 3)
fmt.Println(resultado) // Imprimirá 8
```

## Funciones Anónimas en Go

Las funciones anónimas, también conocidas como funciones lambda, son funciones sin un nombre definido. Puedes declarar y utilizar funciones anónimas en el lugar donde las necesites. Aquí tienes un ejemplo de una función anónima que calcula el cuadrado de un número:

```go
cuadrado := func(x int) int {
  return x * x
}

resultado := cuadrado(5)
fmt.Println(resultado) // Imprimirá 25
```

## Funciones como Tipo de Datos

En Go, las funciones son ciudadanos de primera clase, lo que significa que puedes asignar funciones a variables y pasarlas como argumentos a otras funciones. Esto permite la creación de funciones de orden superior.

```go
func aplicarFuncion(fn func(int) int, x int) int {
  return fn(x)
}

doble := func(x int) int {
  return x * 2
}

resultado := aplicarFuncion(doble, 5)
fmt.Println(resultado) // Imprimirá 10
```

## Funciones con Parámetros del Mismo Tipo

Cuando una función recibe múltiples parámetros del mismo tipo, puedes declararlos de la siguiente manera:

```go
func suma(a, b int) int {
  resultado := a + b
  return resultado
}
```

En este ejemplo, la función `suma` recibe dos parámetros `a` y `b`, ambos de tipo `int`. La declaración simplificada se utiliza para reducir la repetición de tipos de datos en la firma de la función.

## Declaración de Funciones en Go que Retornan Múltiples Valores

En Go, puedes declarar una función que devuelve múltiples valores utilizando la siguiente sintaxis:

```go
func nombreFuncion(parametros) (tipoDeRetorno1, tipoDeRetorno2, ...) {
    // Cuerpo de la función
    // ...
    return valor1, valor2, ...
}
```

Aquí tienes un ejemplo de una función que retorna dos valores: la suma y la resta de dos números enteros:

```go
func operacionesMatematicas(a, b int) (int, int) {
    suma := a + b
    resta := a - b
    return suma, resta
}
```

### Llamada a Funciones que Retornan Múltiples Valores

Para llamar a una función que retorna múltiples valores, puedes asignar los valores de retorno a variables separadas o utilizar la asignación múltiple en una sola línea:

```go
resultadoSuma, resultadoResta := operacionesMatematicas(10, 5)
```

O puedes ignorar uno de los valores utilizando el guion bajo `_`:

```go
resultadoSuma, _ := operacionesMatematicas(10, 5)
```

## Cierre (Closures) en Funciones Anónimas

Las funciones anónimas en Go pueden formar cierres (closures) al capturar variables locales. Esto les permite mantener el estado entre llamadas.

```go
func contador() func() int {
  count := 0
  return func() int {
    count++
    return count
  } 
}

contador1 := contador()
fmt.Println(contador1()) // Imprimirá 1
fmt.Println(contador1()) // Imprimirá 2

contador2 := contador()
fmt.Println(contador2()) // Imprimirá 1
```
