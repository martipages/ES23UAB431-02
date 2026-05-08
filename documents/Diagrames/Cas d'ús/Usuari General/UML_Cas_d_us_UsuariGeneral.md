@startuml
left to right direction

''Perfils:

:Cuiner:

:Client:

:Repartidor:

:Usuari General: as UsuariGeneral

:Usuari No Registrat: as UsuariNoRegistrat

rectangle Accedir {

(Login) as Login

}

rectangle ModificacioPerfil {

(Donar-se de baixa)

(Omplir perfil)

(Modificar perfil)

}

(Vincular Compte Bancari) as VincularCompteBancari


''Herencies:
Client --|> UsuariGeneral

Cuiner --|> UsuariGeneral

Repartidor --|> UsuariGeneral

UsuariNoRegistrat <|-- UsuariGeneral

''Actors Externs:

VincularCompteBancari --> EntitatBancaria

Login --> CorreuElectronic

''Relacions

UsuariGeneral --> VincularCompteBancari

UsuariGeneral --> Login

UsuariGeneral --> (Donar-se de baixa)

UsuariGeneral --> (Omplir perfil)

UsuariGeneral --> (Modificar perfil)

''Include / Extend

@enduml