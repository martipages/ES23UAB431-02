# Especificacions casos d'ús


### CAS D’ÚS: _Demanar ingrés_


## Versió: _1.5_

## Data: _17/05/2026_

## Autors: _Hug Capafons Cuadra_

## Descripció: 
_El cuiner i el repartidor poden demanar l’ingrés dels seus diners._

## Actors: 
_Cuiner, Repartidor, Entitat Bancària_

## Precondició: 
_Han de tenir com a mínim una certa quantitat de diners pendents de cobrar per poder sol·licitar l’ingrés. Si no, va al flux alternatiu No suficients diners per cobrar. A més, ha de tenir associat un compte bancari. Si no, va al flux alternatiu Sense compte bancari._

## Flux principal:
__1. L’usuari entra a un apartat que indica l’històric de comandes i si ja s’han cobrat o no.<br>
2. El sistema calcula automàticament el que falta pendent de cobrar, segons el que ha cuinat/repartit.<br>
3. L’usuari clica el botó de sol·licitar ingrés, que envia la sol·licitud a l’Entitat Bancària per a que se li faci l’ingrés.<br>
4. Finalment, l’usuari rep els diners que se li deuen, totes les comandes pendents de cobrar es marquen com a cobrades i el comptador de diners pendents de cobrar es posa a 0.__

## Subfluxos: _Diferents alternatives dins del flux principal_

## Fluxos alternatius: 
_**No suficients diners per cobrar**
<br>Si l’usuari no arriba al mínim de diners pendents de cobrar, el sistema alerta amb un missatge d’error.<br>
**Sense compte bancari**
<br>Si l’usuari no té un compte bancari associat, es mostra un missatge d’error i se li dona la opció d’anar a associar-lo al perfil. (CU Vincular Compte Bancari)

## Postcondició: 
_Els diners queden ingressats al compte de l’usuari i les comandes pendents de cobrar es marquen com a cobrades._

## Requeriments no funcionals: 

## Prioritat: 
_Normal_

## Comentaris:

