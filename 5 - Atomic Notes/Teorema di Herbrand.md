*tags*: [[TEOREMI AI]] [[AGENTI BASATI SULLA CONOSCENZA]] [[LOGICA DEL PRIMO ORDINE FOL]]

>[!Teorema] Teorema di Herbrand
> Se $KB \models \alpha$ allora c'è una dimostrazione che coinvolge solo un *sottoinsieme finito* dell $KB$ *proposizionalizzata*

>[!question] Perché sottoinsieme **finito** è importante?
> Se, quando si porta una $KB$ da **FOL** a **PROP**, è presente una funzione si possono creare *infinite* istanze. Ad esempio:
> Giovanni, Padre (Giovanni), Padre(Padre(Giovanni)), etc.

>[!hint] A livello operativo...
> Si può procedere incrementalmente
> 1. Creare le istanze con le costanti 
> 2. Creare poi quelle con un solo livello di annidamento: 
> $$Padre(Giovanni), Madre(Giovanni)$$ 
> 3. Poi quelle con due livelli di annidamento: 
> 	$$Padre(Padre(Giovanni)), Padre(Madre(Giovanni)) Madre(Padre(Giovanni)) Madre(Madre(Giovanni)) …$$

> [!attention] Attenzione
> Se $KB \not\models \alpha$ il processo non termina. Il problema è **semidecidibile**.


## Riferimenti utili

* [[Conseguenza logica]]
* [[Trasformazione in Logica Proposizionale]]