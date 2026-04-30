@startuml
left to right direction

:Cuiner:
:Client:
:Repartidor:

Repartidor <|-- Client

rectangle Ingrés {
(Fer pagament) as Pagament
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

Client --> PropPlats
Client --> Pagament
Client --> Xatejar
Client --> Seg
Client --> SubPla
Client --> RepetirPrevies
Client --> Val
Client --> Reserva

GPS --> Seg

Cuiner --> Xatejar

Pagament --> Repartidor
Pagament --> Cuiner
PropPlats --> Cuiner


Xatejar ..> VeureXats : include
Val ..> ConsultarPrevies : include
Reserva ..> Modificar : include
Reserva ..> RepartidorComanda : include
Reserva ..> RepetirPrevies : extend
RepetirPrevies ..> ConsultarPrevies : include

@enduml