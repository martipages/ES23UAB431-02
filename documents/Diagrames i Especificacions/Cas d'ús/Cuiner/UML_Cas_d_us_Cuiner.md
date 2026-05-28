@startuml
left to right direction

''Perfils:

:Cuiner:

:Client:

:Repartidor:

:Usuari General: as UsuariGeneral

''CU:

rectangle Ingrés {

(Fer pagament) as Pagament

}


rectangle ProposarPlats {

(Proposar plats) as PropPlats

}

rectangle Xats {

(Xatejar entre cuiner i client) as Xatejar

(Veure xats) as VeureXats

}


rectangle Ingrés {

(Fer pagament) as Pagament

}


rectangle Comandes {

(Acceptar comandes) as AcceptarComanda

(Veure reserves de comandes) as VeureReserves

}

rectangle Propostes {

(Veure el menú de propostes) as MenúPropostes

(Acceptar proposta de plat) as AcceptarProposta

}

rectangle Perfil {

(Indicar disponibilitat) as Disponibilitat

}

rectangle Xats {

(Xatejar entre cuiner i client) as Xatejar

(Veure xats) as VeureXats

}

rectangle Ingrés {

(Fer pagament) as Pagament

(Vincular compte bancari) as VincularCompteBancari

}

''Herencies:

Repartidor <|-- Cuiner

UsuariGeneral <|-- Client

UsuariGeneral <|-- Repartidor

UsuariGeneral <|-- Cuiner

''Actors Externs:

Pagament --> EntitatBancaria

VincularCompteBancari --> EntitatBancaria

''Relacions

Client --> PropPlats

Client --> Pagament

Client --> VeureXats

Cuiner --> Disponibilitat

Cuiner --> VeureReserves

Cuiner --> MenúPropostes

Cuiner --> VeureXats

Cuiner --> (Oferir conjunt de plats)

Pagament --> Repartidor

Pagament --> Cuiner

PropPlats --> Cuiner

UsuariGeneral --> VincularCompteBancari

''Include / Extend

VeureReserves ..> AcceptarComanda : include

AcceptarProposta ..> AcceptarComanda : extend

Xatejar ..> AcceptarProposta : extend

MenúPropostes ..> AcceptarProposta: include

VeureXats  ..> Xatejar : include
@enduml