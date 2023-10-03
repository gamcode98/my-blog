---
sidebar_position: 15
---

# Uso de Mapas en Go

En este tutorial, exploraremos cómo utilizar mapas en el lenguaje de programación Go. Los mapas son estructuras de datos clave-valor extremadamente versátiles que te permiten asociar valores con claves únicas.

## Declaración de Mapas

En Go, puedes declarar un mapa utilizando la siguiente sintaxis:

```go
nombreMapa := make(map[TipoClave]TipoValor)
```

Por ejemplo, aquí se declara un mapa que relaciona nombres de frutas con sus colores:

```go
frutas := make(map[string]string)
```

## Asignación de Valores a Mapas

```go
frutas["manzana"] = "roja"
frutas["plátano"] = "amarillo"
frutas["uva"] = "morada"
```

## Acceso a Valores en Mapas

Para acceder a los valores en un mapa, simplemente utiliza la clave:

```go
colorManzana := frutas["manzana"]
fmt.Println("El color de la manzana es", colorManzana) // Imprimirá "El color de la manzana es roja"
```

Es importante tener en cuenta que si intentas acceder a una clave que no existe en el mapa, obtendrás un valor cero para el tipo de valor del mapa. En el caso de strings, será una cadena vacía ("").

## Comprobación de la Existencia de Claves

```go
color, existe := frutas["pera"]
if existe {
  fmt.Println("El color de la pera es", color)
} else {
  fmt.Println("La pera no está en el mapa.")
}
```

## Eliminación de Claves en Mapas

Para eliminar una clave y su valor asociado de un mapa, utiliza la palabra clave delete:

```go
delete(frutas, "plátano")
```

## Iteración sobre Mapas

Puedes recorrer un mapa utilizando un bucle for y la palabra clave range. Esto te permite acceder a todas las claves y valores en el mapa:

```go
for clave, valor := range frutas {
  fmt.Printf("La fruta %s es de color %s\n", clave, valor)
}
```

## Mapas de Mapas

Los mapas en Go pueden contener otros mapas como valores. Esto te permite crear estructuras de datos más complejas:

```go
empleados := make(map[int]map[string]string)
empleados[1] = map[string]string{"nombre": "Juan", "puesto": "Gerente"}
empleados[2] = map[string]string{"nombre": "María", "puesto": "Desarrollador"}
```
