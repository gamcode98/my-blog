---
sidebar_position: 14
---

# Recorrido de Slices con `range` en Go

En este tutorial, exploraremos cómo recorrer slices utilizando la palabra clave `range` en el lenguaje de programación Go. La palabra clave `range` es una herramienta útil para iterar sobre los elementos de un slice de manera sencilla y eficiente.

## Uso Básico de `range`

La sintaxis básica de `range` se utiliza en un bucle `for` para recorrer los elementos de un slice:

```go
for índice, valor := range slice {
  // Código para procesar el valor
}
```

- `índice`: Es el índice del elemento actual en el slice.
- `valor`: Es el valor del elemento actual en el slice.

Por ejemplo, aquí hay un código que recorre un slice de números e imprime sus índices y valores:

```go
numeros := []int{10, 20, 30, 40, 50}
for índice, valor := range numeros {
  fmt.Printf("Índice: %d, Valor: %d\n", índice, valor)
}
```

## Ignorar Índices o Valores

Si no necesitas usar el índice o el valor en el bucle for, puedes usar el guión bajo (_) para ignorarlos:

```go
numeros := []int{10, 20, 30, 40, 50}
for _, valor := range numeros {
  fmt.Println(valor)
}
```

## Recorriendo Slices de Strings

`range` también se puede usar para recorrer slices de strings, donde `valor` será el carácter en la posición correspondiente:

```go
texto := "Hola, mundo"
for _, caracter := range texto {
  fmt.Println(string(caracter))
}
```

## Recorriendo Slices de Mapas

Puedes utilizar `range` para recorrer un slice de mapas, donde cada elemento es un mapa:

```go
personas := []map[string]string{
  {"nombre": "Juan", "edad": "30"},
  {"nombre": "María", "edad": "25"},
  {"nombre": "Carlos", "edad": "35"},
}

for _, persona := range personas {
  fmt.Printf("Nombre: %s, Edad: %s\n", persona["nombre"], persona["edad"])
}
```
