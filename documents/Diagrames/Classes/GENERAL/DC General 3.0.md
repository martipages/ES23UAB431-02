@startuml

skinparam groupInheritance 1



skinparam package<<Layout>> {

&#x20; borderColor Transparent

&#x20; backgroundColor Transparent

&#x20; fontColor Transparent

&#x20; stereotypeFontColor Transparent

&#x20; BorderThickness 10

}



namespace Perfils{

class DadesRepartidor

class DadesCuiner

class DadesClient

class DadesUsuariGeneral

}



namespace Comanda {

&#x20;package p2 <<Layout>>{

class DadesComanda

class DadesPagament

class DadesEnviament

}

}



namespace Menú {

class Plat

class Ingredient

}



namespace Xats {

&#x20;package p1 <<Layout>>{

class Xat

}

class Missatge

} 



DadesUsuariGeneral <|-down- DadesRepartidor

DadesUsuariGeneral <|-down- DadesCuiner

DadesUsuariGeneral <|-down- DadesClient



DadesComanda "1" -right- "1" DadesPagament

DadesComanda "1" -left- "1" DadesEnviament



DadesComanda -- Xat



DadesCuiner "1" -down- "1.." Plat

DadesClient "1" --down-- "    0..\*" DadesComanda

DadesRepartidor "1" --down-- "0..\*" DadesEnviament

DadesCuiner "1" -down- "          0..3" DadesComanda

Plat "1" -up-o "0..\*" DadesComanda

Xat "   1" \*- "1..\*" Missatge

Plat "1" o-- "1..\*" Ingredient

@enduml

