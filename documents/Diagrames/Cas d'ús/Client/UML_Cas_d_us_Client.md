@startuml

left to right direction



''Perfils:



:Cuiner:



:Client:



:Repartidor:



:Usuari General: as UsuariGeneral



:Entitat Bancaria: as EntitatBancaria



''CU:



rectangle Ingrés {



(Fer pagament) as Pagament



}



rectangle ProposarPlats {



(Proposar plats) as PropPlats



}



rectangle FerComanda {



(Fer comandes) as Reserva



(Modificar ingredients adicionals) as Modificar



(Escollir qui reparteix) as RepartidorComanda



(Triar data i hora) as DyT



}



rectangle Xats {



(Xatejar entre cuiner i client) as Xatejar



(Veure xats) as VeureXats



}



rectangle ComandesPrèvies {



(Consultar comandes prèvies) as ConsultarPrevies



(Repetir comandes prèvies) as RepetirPrevies



}





(Seguiment de la comanda) as Seg





rectangle Valoracio {



(Valorar comandes) as Val



}



rectangle Subscripció {



(Subscripció pla mensual) as SubPla



}





''Herencies:

Repartidor <|-- Client



UsuariGeneral <|-- Client



UsuariGeneral <|-- Repartidor





''Actors Externs:



GPS <-- Seg



Pagament --> EntitatBancaria



''Relacions



Client --> PropPlats



Client --> Pagament



Client --> Seg



Client --> SubPla



Client --> ConsultarPrevies



Client --> Val



Client --> Reserva



Client --> VeureXats



Pagament --> Repartidor



Pagament --> Cuiner



PropPlats --> Cuiner



Cuiner --> VeureXats



Seg --> Repartidor



''Include / Extend



Val ..> ConsultarPrevies : include



Reserva ..> Modificar : include



Reserva ..> RepartidorComanda : include



Reserva ..> DyT : include



Reserva ..> RepetirPrevies : extend



ConsultarPrevies <.. RepetirPrevies : extend



VeureXats  ..> Xatejar : include

@enduml

