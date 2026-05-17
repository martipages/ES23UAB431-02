# Especificacions casos d'ús


### CAS D’ÚS: _Fer pagament_


## Versió: _1.0_

## Data: _17/05/2026_

## Autors: _Hug Capafons Cuadra_

## Descripció: 
_El client realitza el pagament d'una comanda._

## Actors: 
_Client, entitat bancària_

## Precondició: 
_El client ha d'estar realitzant una comanda._

## Flux principal: _Flux principal d’events del cas d’ús_
_1. El client emet el pagament de l'improt de la comanda a l'entiat bancària. <br>
 2. L'entiat bancària autentifica el pagament.<br>
	2.1. Si el pagament és vàlid, la comanda consta com a pagada. 
	2.2. Els diners del pagament arriben al compte associat a l'aplicació (no directament al cuiner o el repartidor)._
 
## Subfluxos:
_Si l'usuari ho deistja, pot cancelar el pagament abans de fer-lo._ <br>

## Fluxos alternatius: _Variacions en els fluxos principals o casos d’excepció_
_Si el pagament no és vàlid, l'aplicació el tornarà a demanar, fins que sigui vàlid<br>_

## Postcondició: 
_Si l'usuari no ha cancelat i tot ha sortit bé, la comanda constarà com a pagada._

## Requeriments no funcionals: 
_Decisió de dissney: El pagament es farà amb targeta o payPal
Interfícies externes: Quan es faci el pagament s'haurà de connectar amb l'entitat bancària
Restricció de disseny de seguretat: S'haurà de autentificar el pagament_

## Prioritat: 
_Normal_

## Comentaris:


