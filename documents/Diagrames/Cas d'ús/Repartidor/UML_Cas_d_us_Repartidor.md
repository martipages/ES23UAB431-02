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





(Seguiment de la comanda) as Seg



(Vincular Compte Bancari) as VincularCompteBancari



rectangle Ingrés {



(Fer pagament) as Pagament



}



rectangle RepartirComandes {



(Acceptar comandes a repartir) as AcceptarComandes



(Veure comandes pendents a repartir) as VeureComandes



}







''Herencies:



Repartidor <|-- Client



Repartidor <|-- Cuiner



UsuariGeneral <|-- Client



UsuariGeneral <|-- Repartidor



UsuariGeneral <|-- Cuiner



''Actors Externs:



Seg --> GPS



Pagament --> EntitatBancaria



''Relacions



Client --> Pagament



Client --> Seg



Repartidor --> VeureComandes



UsuariGeneral --> VincularCompteBancari



VincularCompteBancari --> EntitatBancaria



Pagament --> Repartidor



Seg --> Repartidor



''Include / Extend





VeureComandes <.. AcceptarComandes : extend



@enduml

