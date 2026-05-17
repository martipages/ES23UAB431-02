# Especificacions casos d'ús


### CAS D’ÚS: _Repetir comandes prèvies_


## Versió: _1.0_

## Data: _17/05/2026_

## Autors: _Hug Capafons Cuadra_

## Descripció: 
_El client pot repetir una comanda prèvia, en cas que estigui disponible_

## Actors: 
_Client_

## Precondició: 
_La comanda prèvia que es vol repetir ha d'estar disponible._

## Flux principal: 
_**Extensions point:** CU consultar comandes prèvies. 
 1. Es selecciona la comanda prèvia disponible.<br>
 2. Es crea una nova instància de comanda amb alguns atributs copiats de l'anterior, però altres no (com la data)_<br>

## Subfluxos: 
_**Extension point:** Cu consultar ocmandes prèvies.
Si no s'ha fet cap comanda, no es podrà veure cap comanda prèvia.<br>

Si cap comanda prèvia està disponible, no es podrà repetir.<br>
_

## Fluxos alternatius: 

## Postcondició: 
_El client tindrà una nova comanda activa._

## Requeriments no funcionals: 
_Restricció de rendiment estàtic: Cada client té un màxim de 3 comandes actives simultànices_

## Prioritat: 
_no prioritari_

## Comentaris: 

