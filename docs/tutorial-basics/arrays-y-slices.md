---
sidebar_position: 13
---

# Tutorial: Uso de Arrays y Slices en Go

En este tutorial, exploraremos el uso de arrays y slices en el lenguaje de programación Go. Los arrays y slices son estructuras de datos fundamentales que se utilizan para almacenar colecciones de elementos en Go.

## Arrays en Go

Un array en Go es una colección ordenada de elementos del mismo tipo con un tamaño fijo. La declaración de un array se realiza de la siguiente manera:

```go
var nombreArray [tamaño]tipo
```

Por ejemplo, aquí se declara un array de enteros con un tamaño de 5:

```go
var numeros [5]int
```

Puedes asignar valores a un array utilizando índices y accediendo a elementos específicos:

```go
numeros[0] = 10
numeros[1] = 20
```

También puedes inicializar un array al declararlo:

```go
numeros := [5]int{10, 20, 30, 40, 50}
```

## Slices en Go

Un slice en Go es una vista dinámica de un array, lo que significa que puede tener un tamaño variable. La declaración de un slice se hace de la siguiente manera:

```go
nombreSlice := []tipo{}
```

Por ejemplo, aquí se declara un slice de enteros:

```go
numeros := []int{10, 20, 30, 40, 50}
```

Puedes agregar elementos a un slice utilizando la función `append`:

```go
numeros = append(numeros, 60)
```

También puedes crear un slice a partir de un array existente utilizando la notación de índices:

```go
array := [5]int{10, 20, 30, 40, 50}
slice := array[1:4] // Crea un slice que incluye los elementos 20, 30 y 40
```

## Longitud y Capacidad de Slices

Un slice tiene dos propiedades importantes: longitud (len) y capacidad (cap). La longitud es la cantidad de elementos en el slice, mientras que la capacidad es la cantidad de elementos que el slice puede contener en el array subyacente.

```go
slice := []int{10, 20, 30, 40, 50}
fmt.Println(len(slice)) // Imprimirá 5 (longitud)
fmt.Println(cap(slice)) // Imprimirá 5 (capacidad)
```

## Slices en Rangos

Los slices pueden crearse utilizando la notación de rangos para acceder a un subconjunto de un slice existente:

```go
sliceOriginal := []int{10, 20, 30, 40, 50}
subSlice := sliceOriginal[1:4] // Crea un slice que incluye los elementos 20, 30 y 40
```

La notación 1:4 se descompone de la siguiente manera:

- El número antes de los dos puntos (1) representa el índice de inicio (inclusivo).
- El número después de los dos puntos (4) representa el índice de finalización (exclusivo).
- Esto significa que el slice resultante incluirá todos los elementos desde el índice de inicio hasta el índice de finalización, pero el elemento en el índice de finalización no se incluirá en el slice.

## Notaciones en la manipulación de slices

### Notación [inicio:fin]

- `inicio`: Índice del primer elemento incluido en el slice (inclusive).
- `fin`: Índice del elemento después del último elemento incluido en el slice (exclusivo).

```go
sliceOriginal := []int{10, 20, 30, 40, 50}
subSlice := sliceOriginal[1:4] // Crea un slice que incluye los elementos 20, 30 y 40
```

### Notación [:fin]

- Si omites el índice de inicio, se asume que es 0.
- `fin`: Índice del elemento después del último elemento incluido en el slice (exclusivo).

```go
sliceOriginal := []int{10, 20, 30, 40, 50}
subSlice := sliceOriginal[:3] // Crea un slice que incluye los elementos 10, 20 y 30
```

### Notación [inicio:]

- `inicio`: Índice del primer elemento incluido en el slice (inclusive).
- Si omites el índice de fin, se asume que es la longitud máxima del slice o array.

```go
sliceOriginal := []int{10, 20, 30, 40, 50}
subSlice := sliceOriginal[2:] // Crea un slice que incluye los elementos desde 30 hasta el final
```

### Notación [:]

- Si omites tanto el índice de inicio como el de fin, se copia el slice completo.

```go
sliceOriginal := []int{10, 20, 30, 40, 50}
copiaSlice := sliceOriginal[:] // Crea una copia completa del sliceOriginal
```

### Notación [inicio:fin:max]

- `inicio`: Índice del primer elemento incluido en el slice (inclusive).
- `fin`: Índice del elemento después del último elemento incluido en el slice (exclusivo).
- `max`: Capacidad máxima del slice (opcional).

Esta notación te permite especificar la capacidad máxima del slice, que es útil para controlar la longitud y la capacidad del slice resultante.

```go
sliceOriginal := []int{10, 20, 30, 40, 50}
subSlice := sliceOriginal[1:4:4] // Crea un slice que incluye los elementos 20, 30 y 40, con una capacidad máxima de 4
```

Estas notaciones te permiten crear slices flexibles y cómodos en Go para manipular colecciones de datos de manera efectiva. Cada notación se adapta a diferentes situaciones, ya sea para crear subconjuntos, copias o controlar la capacidad máxima del slice resultante.

## Concatenación de Slices en Go

En Go, puedes concatenar dos slices utilizando el operador `...`. Esto te permite combinar dos slices en uno solo. Aquí tienes un ejemplo:

```go
slice1 := []int{1, 2, 3}
slice2 := []int{4, 5, 6}

concatenado := append(slice1, slice2...) // Utiliza el operador '...' para concatenar los slices
fmt.Println(concatenado) // Imprimirá [1 2 3 4 5 6]
```

En este ejemplo, hemos concatenado `slice1` y `slice2` en `concatenado` utilizando el operador `...` dentro de la función `append`. El resultado es un nuevo slice que contiene todos los elementos de ambos slices originales.

Recuerda que el operador `...` se utiliza para desempaquetar un slice al pasar sus elementos como argumentos individuales a una función var iádica como `append`. Esto es especialmente útil cuando deseas concatenar slices.

La concatenación de slices es una técnica común en Go cuando necesitas combinar o ampliar colecciones de datos de manera eficiente.
