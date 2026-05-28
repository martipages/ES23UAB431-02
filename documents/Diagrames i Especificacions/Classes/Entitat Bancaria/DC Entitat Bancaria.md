@startuml
skinparam groupInheritance 1

skinparam package<<Layout>> {
  borderColor Transparent
  backgroundColor Transparent
  fontColor Transparent
  stereotypeFontColor Transparent
  BorderThickness 10
}

namespace Persones #DDDDDD {
class DadesCuiner
class DadesUsuariGeneral
class DadesClient
class CompteBancari
class DadesRepartidor
}

class interficieEntitatBancaria

DadesUsuariGeneral <|-- DadesCuiner
DadesUsuariGeneral <|-- DadesClient
DadesUsuariGeneral <|-- DadesRepartidor

DadesCuiner -- interficieEntitatBancaria
DadesClient -- interficieEntitatBancaria
DadesRepartidor -- interficieEntitatBancaria

DadesUsuariGeneral - CompteBancari

@enduml