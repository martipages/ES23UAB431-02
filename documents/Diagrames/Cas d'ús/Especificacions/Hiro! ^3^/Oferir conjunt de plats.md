# Especificacions casos d'ús


### CAS D’ÚS: _Oferir conjunt de plats_


## Versió: _1.0_

## Data: _14/05/2026_

## Autors: _Martí Pagès Sánchez_

## Descripció: _Aquest cas d’ús descriu com el cuiner publica els diferents plats proposats per ell mateix._

## Actors: _Cuiner_

## Precondició: 

## Flux principal: _1. El cuiner veu el menú de vista de plats que s’ofereixen actualment.<br>
2. El cuiner crea una instància de plat, que inicialment serà buit.<br>
3. El cuiner podrà editar la seva informació (nom, descripció i ingredients), sent tant detallat com vulgui.<br>
4. Es retornarà al menú de vista de plats, on es permetrà tornar a afegir un plat._

## Subfluxos: _**Publicar imatges**<br>
Si així ho desitja, el cuiner pot publicar una o diverses imatges del plat en qüestió.<br>
**Marcar ingredients com a opcionals**<br>
Si escau, el cuiner podrà marcar certs ingredients com a opcionals._

## Fluxos alternatius: _**Mateix nom**
Si un plat existent té el mateix nom que el que indica el plat nou, en intentar guardar-lo, sortirà una notificació avisant que un altre plat ja té aquest nom, no deixant-lo guardar i instant a canviar el nom d’aquest nou plat._

## Postcondició: _El plat quedarà afegit dins la llista de plats que aquell cuiner ofereix._

## Requeriments no funcionals: _RNF-6-01 (Control accés menú)_

## Prioritat: _Normal_

## Comentaris: 

