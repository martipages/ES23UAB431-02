@startuml
skinparam groupInheritance 1

namespace Persones #DDDDDD {
class DadesCuiner
class DadesUsuariGeneral
class DadesClient
class CompteBancari
}

namespace Comandes {
 namespace Xats #DDDDDD {
  class Xat
  class Missatge
 }
  class Plat
  class Comanda
}

DadesUsuariGeneral <|-- DadesCuiner
DadesUsuariGeneral <|-- DadesClient

DadesUsuariGeneral - CompteBancari

DadesCuiner "1" -- "1..*" Plat
DadesClient "1" - "0..3" Comanda
Plat "1..*" -- "0..*" Comanda
Comanda - Xat
Xat "1" *-- "1..*" Missatge
@enduml