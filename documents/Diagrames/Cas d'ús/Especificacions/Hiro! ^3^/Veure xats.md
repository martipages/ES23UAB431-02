# Especificacions casos d'ús


### CAS D’ÚS: _Veure xats_


## Versió: _1.0_

## Data: _14/05/2026_

## Autors: _Martí Pagès Sánchez_

## Descripció: 
_Aquest cas d’ús descriu com el cuiner i el client veuen els xats que tenen entre ells._

## Actors: 
_Client, Cuiner_

## Precondició: 
_Ha d’haver-hi com a mínim un xat actiu. Si no, va al flux alternatiu “No hi ha xats actius”._

## Flux principal: 
_1. L’usuari fa clic sobre la pestanya de xats.<br>
2. El sistema mostra l’històric de xats actius amb la seva comanda associada, permetent entrar a cadascun.<br>
        2.1. Si l’usuari ho desitja, pot entrar en un xat._

## Subfluxos: 

## Fluxos alternatius: 
_**No hi ha xats actius**
Si no hi ha xats actius (l’usuari ha tingut 0 xats), es mostra un missatge d’error (tipus: “Vaja… Sembla ser que no tens cap xat iniciat. Torna quan en tinguis algun!”)._

## Postcondició: 
_El sistema resta a la pantalla de xats, on apareixen tots els xats actius._

## Requeriments no funcionals:

## Prioritat: 
_Normal_

## Comentaris: 

