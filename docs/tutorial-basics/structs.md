---
sidebar_position: 16
---

# Uso de Structs en Go

En este tutorial, exploraremos cómo utilizar estructuras (structs) en el lenguaje de programación Go. Las structs son tipos de datos personalizados que te permiten combinar diferentes tipos de datos bajo una única entidad (es la forma de hacer clases en Go).

## Declaración de Structs

Puedes declarar una estructura en Go utilizando la siguiente sintaxis:

```go
type NombreStruct struct {
    Campo1 Tipo1
    Campo2 Tipo2
    // Otros campos
}
```

Por ejemplo, aquí se declara una estructura llamada `Persona` con dos campos, `Nombre` y `Edad`:

```go
type Persona struct {
  Nombre string
  Edad   int
}
```

## Creación de Instancias de Structs

Para crear una instancia de una estructura, simplemente utiliza la sintaxis de inicialización de estructuras:

```go
persona1 := Persona{"Juan", 30}
persona2 := Persona{Nombre: "María", Edad: 25}
```

Puedes crear una instancia de estructura sin especificar todos los campos, en cuyo caso se utilizarán los valores predeterminados:

```go
persona3 := Persona{Nombre: "Carlos"}
```

## Acceso a Campos de Structs

Para acceder a los campos de una estructura, utiliza la notación de punto (`.`):

```go
fmt.Println(persona1.Nombre) // Imprime "Juan"
fmt.Println(persona2.Edad)   // Imprime 25
```

## Modificación de Campos de Structs

Puedes modificar los campos de una estructura directamente:

```go
persona1.Edad = 31
```

## Estructuras Anidadas

Las estructuras en Go también pueden estar anidadas, lo que significa que puedes tener estructuras dentro de otras estructuras:

```go
type Direccion struct {
  Calle     string
  Ciudad    string
  Provincia string
}

type Contacto struct {
  Email    string
  Telefono string
  Direccion
}
```

En este ejemplo, la estructura `Contacto` contiene un campo de tipo `Direccion`.
