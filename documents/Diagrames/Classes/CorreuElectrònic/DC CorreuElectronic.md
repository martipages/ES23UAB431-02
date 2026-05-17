@startuml

skinparam groupInheritance 1

namespace Persones #DDDDDD {

class DadesCuiner

class DadesRepartidor

class DadesUsuariGeneral

class DadesClient

class DadesUsuariNoRegistrat

class CorreuElectronic

}



DadesUsuariNoRegistrat <|-- DadesUsuariGeneral

DadesUsuariGeneral <|-- DadesCuiner

DadesUsuariGeneral <|-- DadesClient

DadesUsuariGeneral <|-- DadesRepartidor

DadesUsuariGeneral - CorreuElectronic

DadesUsuariNoRegistrat - CorreuElectronic



@enduml

