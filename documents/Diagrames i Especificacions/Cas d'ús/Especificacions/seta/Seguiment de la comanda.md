# Especificacions casos d'ús


### CAS D’ÚS: _Seguiment de la comanda_


## Versió: _1.0_

## Data: _14/05/2026_

## Autors: _Hug Capafons Cuadra_

## Descripció: 
_El client pot rastrejar la ubicació geogràfica de la seva comanda_ 

## Actors: 
_Client, GPS, Repartidor_

## Precondició: 
_La comanda ha d'estar pagada i repartint-se._

## Flux principal: 
_1. El client accedeix a la comanda desde la llista de comandes actives <br>
2. Si el repartidor ja està repartint la comanda, podrà accedir a la finstra de google maps de la pàgina web
per seguir la ubicació del repartidor en temps real._ <br>

## Subfluxos: 
## Fluxos alternatius:
**Fluxos alternatius**
_Si la comanda no està sent repartida (encara s'està cuinant) no es podrà veure la seva ubicació._

## Postcondició:

## Requeriments no funcionals: 
_RNF-3-01 (Accés a seguiment)
RNF-3-02 (Mapa utilitza Google Maps)_

## Prioritat: 
_Normal_

## Comentaris: 

