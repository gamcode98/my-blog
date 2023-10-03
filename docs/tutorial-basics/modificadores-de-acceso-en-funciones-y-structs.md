---
sidebar_position: 17
---

# Reglas de Visibilidad en Go

En Go, no existen modificadores de acceso como en otros lenguajes. En su lugar, las reglas de visibilidad se basan en convenciones de nombres simples. En este tutorial, aprenderemos cómo funcionan estas reglas y cómo controlar la visibilidad de campos y funciones en Go.

## Reglas de Visibilidad Básicas

En Go, el principio general es que los nombres que comienzan con una letra mayúscula son públicos y exportables (accesibles desde fuera del paquete), mientras que los nombres que comienzan con una letra minúscula son privados y no exportables (accesibles solo dentro del paquete).

### Campos de Structs

```go
type Persona struct {
    Nombre string    // Público
    edad   int       // Privado
}
```

En este ejemplo, `Nombre` es público y puede ser accedido desde fuera del paquete, mientras que `edad` es privado y solo puede ser accedido dentro del paquete donde se define.

## Funciones

```go
func ObtenerNombre(p Persona) string { // Público
    return p.Nombre
}

func calcularEdad(p Persona) int { // Privado
    return p.edad
}
```

`ObtenerNombre` es una función pública y puede ser utilizada desde fuera del paquete, mientras que `calcularEdad` es una función privada y solo puede ser utilizada dentro del paquete donde se define.

## Exportando Nombres

Si deseas que un nombre sea accesible desde fuera del paquete, simplemente asegúrate de que comience con una letra mayúscula.

### Ejemplo de Exportación

```go
type Producto struct {
    Nombre     string // Público
    precio     float64 // Privado
}

func NuevoProducto(nombre string, precio float64) Producto { // Pública
    return Producto{Nombre: nombre, precio: precio}
}
```

En este ejemplo, `Producto` y `NuevoProducto` son exportables porque comienzan con letras mayúsculas. Los campos de `Producto` que comienzan con minúsculas son privados por convención.

## Acceso y Visibilidad

El acceso a los campos y funciones en Go está determinado por las reglas de visibilidad basadas en convenciones de nombres. Esto fomenta la claridad y simplicidad en el diseño de paquetes y estructuras de datos.
