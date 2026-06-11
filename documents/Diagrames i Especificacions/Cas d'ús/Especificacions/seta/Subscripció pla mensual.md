# Especificacions casos d'ús


### CAS D’ÚS: _Subscripció al plà mensual_


## Versió: _1.0_

## Data: _17/05/2026_

## Autors: _Hug Capafons Cuadra_

## Descripció: 
_El client es podrà subscriure a un plà mensual. El plà conté una tarifa plana d'enviaments i un sistema de punts_

## Actors: 
_Client_

## Precondició: 
_El client ha d’estar registrat com a client i amb un compte bancari vàlid associat_

## Flux principal: 
_Dins del perfil, el client pot modificar la seva subscripció al pla mensual. Pot activar-la o donar-se de baixa.._

## Subfluxos: 
**Import mensual**
Mentre estigui activada, ingressarà mitjançant l’entitat bancaria 5€ al mes.

## Fluxos alternatius: 
**No registrat**
Si no està registrat i amb un compte bancari vàlid associat apareixerà un missatge d’error dient 
“No es pot efectuar la subscripció perquè no estàs registrat o no tens un compte bancari vàlid”.


## Postcondició: 
L’usuari constarà com a inscrit al plà mensual.

## Requeriments no funcionals: 

## Prioritat: 
_No prioritari_

## Comentaris: 

