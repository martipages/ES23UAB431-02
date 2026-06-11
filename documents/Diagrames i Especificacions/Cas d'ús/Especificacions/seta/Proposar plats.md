# Especificacions casos d'ús


### CAS D’ÚS: _Proposar plats_


## Versió: _1.0_

## Data: _17/05/2026_

## Autors: _Hug Capafons Cuadra_

## Descripció: 
_El client pot proposar plats a un  cuiner sempre i quan estigui disponible._

## Actors: _Client, Cuiner_

## Precondició: 
_El cuiner ha d'estar disponible_

## Flux principal: 
_1. El cuiner accedeix a la llista de cuiners disponibles<br>
2. En cas que n'hi hagi algun, podrà proposar-li un plat per a que li faci<br>
3. El cuiner podrà acceptar-lo o no acceptarlo (cas d'ús propi)<br>
4. Si el cuiner l'accepta, es crearà una instància nova de plat en una comanda i si li notificarà al client. Passarà a ser una comanda activa_


## Subfluxos: 
**Cuiner no accepta**
_Si el cuiner rebutja el plat, se li notifacrà al client._
## Fluxos alternatius:
**Cuiner no disponible**
_Si no hi ha cap cuiner disponible, no es podràn proposar plats._

## Postcondició: 

## Requeriments no funcionals: 
_RNF-2-02: (Màxim 3 comandes actives simultàniament)
RNF-6-01: (Els cuiners són els únics que poden accedir a aquest menú específic)_

## Prioritat: 
_No prioritari_

## Comentaris: 


