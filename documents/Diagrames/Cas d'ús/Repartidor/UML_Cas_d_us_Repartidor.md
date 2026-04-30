@startuml
left to right direction

:Cuiner:
:Client:
:Repartidor:

Repartidor <|-- Client
Repartidor <|-- Cuiner

rectangle Ingrés {
(Fer pagament) as Pagament
}
rectangle RepartirComandes {
(Acceptar comandes a repartir) as AcceptarComandes
(Veure comandes pendents a repartir) as VeureComandes
}

Client --> Pagament
Pagament --> Repartidor
Repartidor --> AcceptarComandes

AcceptarComandes ..> VeureComandes : include

@enduml