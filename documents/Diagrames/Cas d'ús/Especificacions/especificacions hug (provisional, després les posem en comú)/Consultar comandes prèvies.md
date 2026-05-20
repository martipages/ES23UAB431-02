# Especificacions casos d'ús


### CAS D’ÚS: _Consultar comandes prèvies_


## Versió: _1_.0_

## Data: _16/05/2026_

## Autors: _Hug Capafons Cuadra_

## Descripció: 
_El client pot consultar la llista de comandes prèvies_

## Actors: 
_Client_

## Precondició:
_El client ha de tenir com a mínim una comanda ja feta per a poder consultar-la_

## Flux principal: 
_1. El client accedeix a la llista a la llista de comandes ja realitzades i que ja no estàn actives.<br>
2. Pot veure la llista de comandes ja realitzades. _<br>

## Subfluxos: 
_Al consultar cada comanda ,es podrà veure si està disponible. <br>
Si està disponible, es podrà repetir la comanda (tornar-la a demanar). Si no, no._ <br>
## Fluxos alternatius: _Variacions en els fluxos principals o casos d’excepció_
_Si no existeixen comandes prèvies, no es podrà consultar res._

## Postcondició: 
_En pantalla estaràn les comandes prèvies, en cas que n'hi hagin._
## Requeriments no funcionals: 

## Prioritat: 
_No prioritari_

## Comentaris: 

