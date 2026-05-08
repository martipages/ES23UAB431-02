@startuml
left to right direction

''Perfils:

:Usuari General: as UsuariGeneral

:Usuari No Registrat: as UsuariNoRegistrat

''CU:

rectangle Accedir {

(Login) as Login

(Registrar-se) as Registrar

}

''Herencies:

UsuariGeneral <|-- Cuiner

UsuariNoRegistrat <|-- UsuariGeneral

''Actors Externs:

Registrar --> CorreuElectronic

Login --> CorreuElectronic

''Relacions

Cuiner --> (Oferir conjunt de plats)

UsuariNoRegistrat --> (ConsultarMenu)

UsuariNoRegistrat --> Registrar

UsuariNoRegistrat --> (Cercar)

UsuariGeneral --> Login

(Cercar) --> Cuiner

''Include / Extend

@enduml