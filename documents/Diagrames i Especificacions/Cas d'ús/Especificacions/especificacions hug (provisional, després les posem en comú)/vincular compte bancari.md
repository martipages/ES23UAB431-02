# Especificacions casos d'ús


### CAS D’ÚS: _Vincular Compte Bancari_


## Versió: _1.5_

## Data: _17/05/2026_

## Autors: _Hug Capafons Cuadra_

## Descripció: 
_L’usuari general pot vincular el seu compte bancari._

## Actors: 
_Usuari General_

## Precondició: 
_L’usuari ha d’estar identificat amb el seu DNI. Si no, va al flux alternatiu Falta DNI._

## Flux principal: 
_1. L’usuari entra al seu perfil, on hi ha l’apartat de “Compte Bancari”.<br>
2. L’usuari pot introduïr o modificar el seu IBAN, i queda guardat per a posteriors operacions. Si l’IBAN no és vàlid, va al flux alternatiu IBAN no vàlid_

## Subfluxos:


## Fluxos alternatius: 
_**Falta DNI**
<br>Si l’usuari no té un DNI associat, surt un missatge d’error, i s’insta a l’usuari a que l’introdueixi.<br>
**IBAN no vàlid**
<br>Es torna a demanar d’introduïr el IBAN_

## Postcondició:
_El compte bancari queda guardat i associat al perfil per a posteriors operacions._

## Requeriments no funcionals: 
_RNF-4-01 el pagament es podrà fer amb targeta bancària o PayPal.
RNF-4-02 Haurà connexió amb Entitat de pagament
RNF-4-03 Autenticació de pagament_

## Prioritat: 
_Normal_

## Comentaris:

