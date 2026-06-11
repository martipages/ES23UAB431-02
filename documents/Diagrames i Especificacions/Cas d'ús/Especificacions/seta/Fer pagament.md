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
3. Si el pagament és vàlid, la comanda consta com a pagada. 
4. Els diners del pagament arriben al compte associat a l'aplicació (no directament al cuiner o el repartidor)._
 
## Subfluxos:
**Cancelar pagament**
_Si l'usuari ho deistja, pot cancelar el pagament abans de fer-lo.<br>_

## Fluxos alternatius: _Variacions en els fluxos principals o casos d’excepció_
**Pagament no vàlid**
_Si el pagament no és vàlid, l'aplicació el tornarà a demanar, fins que sigui vàlid<br>_

## Postcondició: 
_Si l'usuari no ha cancelat i tot ha sortit bé, la comanda constarà com a pagada._

## Requeriments no funcionals: 
_RNF-4-01: El pagament es farà amb targeta o PayPal.
RNF-4-02: Quan es faci el pagament s'haurà de connectar amb l'entitat bancària.
RNF-4-03: S'haurà d’autentificar el pagament._

## Prioritat: 
_Urgent_

## Comentaris:


