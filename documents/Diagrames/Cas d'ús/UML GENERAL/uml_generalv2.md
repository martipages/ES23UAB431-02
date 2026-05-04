@startuml

left to right direction

''Perfils:

:Cuiner:

:Client:

:Repartidor:

:Usuari General: as UsuariGeneral

:Usuari No Registrat: as UsuariNoRegistrat

''CU:

rectangle Ingrés {

(Fer pagament) as Pagament

}

rectangle Accedir {

(Login) as Login

(Registrar-se) as Registrar

}

rectangle ProposarPlats {

(Proposar plats) as PropPlats

}

rectangle FerComanda {

(Reservar comandes) as Reserva

(Modificar ingredients adicionals) as Modificar

(Escollir qui reparteix) as RepartidorComanda

}

rectangle Xats {

(Xatejar entre cuiner i client) as Xatejar

(Veure xats) as VeureXats

}

rectangle ComandesPrèvies {

(Consultar comandes prèvies) as ConsultarPrevies

(Repetir comandes prèvies) as RepetirPrevies

}

rectangle Seguiment {

(Seguiment de la comanda) as Seg

}

rectangle Valoracio {

(Valorar comandes) as Val

}

rectangle Subscripció {

(Subscripció pla mensual) as SubPla

}

rectangle Ingrés {

(Fer pagament) as Pagament

}

rectangle RepartirComandes {

(Acceptar comandes a repartir) as AcceptarComandes

(Veure comandes pendents a repartir) as VeureComandes

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

Repartidor <|-- Client

Repartidor <|-- Cuiner

UsuariGeneral <|-- Client

UsuariGeneral <|-- Repartidor

UsuariGeneral <|-- Cuiner

UsuariNoRegistrat <|-- UsuariGeneral

''Actors Externs:

Seg --> GPS

Pagament --> EntitatBancaria

Registrar --> CorreuElectronic

Login --> CorreuElectronic

''Relacions

Client --> PropPlats

Client --> Pagament

Client --> Seg

Client --> SubPla

Client --> ConsultarPrevies

Client --> Val

Client --> Reserva

Client --> Xatejar

Repartidor --> VeureComandes

UsuariGeneral --> VincularCompteBancari

UsuariGeneral --> Login

UsuariGeneral --> (Donar-se de baixa)

UsuariGeneral --> (Omplir perfil)

Cuiner --> Disponibilitat

Cuiner --> VeureReserves

Cuiner --> MenúPropostes

Cuiner --> Xatejar

Cuiner --> (Oferir conjunt de plats)

UsuariNoRegistrat --> (ConsultarMenu)

UsuariNoRegistrat --> Registrar

UsuariNoRegistrat --> (Cercar)

(Cercar) --> Cuiner

Pagament --> Repartidor

Pagament --> Cuiner

PropPlats --> Cuiner

''Include / Extend

Val ..> ConsultarPrevies : include

Reserva ..> Modificar : include

Reserva ..> RepartidorComanda : include

Reserva ..> RepetirPrevies : extend

ConsultarPrevies ..> RepetirPrevies : include

VeureReserves ..> AcceptarComanda   : include

AcceptarProposta ..> AcceptarComanda : extend

Xatejar ..> AcceptarProposta : extend

MenúPropostes  ..> AcceptarProposta: include

Xatejar ..> VeureXats : include

VeureComandes ..> AcceptarComandes : include

(Omplir perfil) ..> (Modificar perfil) : include

@enduml