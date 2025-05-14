# Reto 2 diagrama 
1 . Elija un problema de la vida real (sistema de gestión de biblioteca, negocio de compra-venta, automóvil, etc) que se pueda modelar a través de objetos y clases. Plantee las relaciones de clases, composiciones, propiedades y comportamientos del sistema en uno mas diagramas tipo UML.

```mermaid
classDiagram
        Muebles <|-- sillas
        Muebles <|-- mesa
        Muebles <|-- cama
        Muebles : +int peso
        Muebles : +bool decorativo
        Muebles: +int precio
        Muebles: +string color
        class mesa {
          +apoyarobjetos()
          +limpiar()
          +cambiarmantel()
          +float distanciapiso-mesa
          +float radio-mesa
        }
        class sillas {
          +float distanciapiso-silla
          +sentarse()
        }
        class cama {
          +str tipocolchon
          +acostarse()
          +tendercama()
        }
    sillas"2" --> "1" mesa : acomodar()
    mesa"2"-->"1"cama:mesadenoche
```
