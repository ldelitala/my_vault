
_tags_: [[DEFINIZIONI]] [[AGENTI BASATI SULLA RICERCA]]

> [!Definizione]  Algoritmi di ricerca informata
> Gli **algoritmi di ricerca informata** (o **euristica**) utilizzano **informazioni aggiuntive sul problema** per **guidare la ricerca** verso la soluzione più promettente.  
> Questa informazione è fornita da una **funzione euristica** ( h(n) ), che stima il **costo rimanente** per raggiungere l’obiettivo dallo stato ( n ).

### Caratteristiche principali
1. Usano una **funzione di valutazione** per scegliere quali stati espandere.
2. Possono essere **più efficienti** perché riducono la parte esplorata dello spazio degli stati.    
3. L’**accuratezza dell’euristica** influenza fortemente le prestazioni.
### Esempi

|Algoritmo|Funzione usata|Completezza|Ottimalità|
|---|---|---|---|
|**Greedy Best-First Search**|( f(n) = h(n) )|✅ (in spazi finiti)|❌|
|**A***|( f(n) = g(n) + h(n) )|✅|✅ (se ( h(n) ) ammissibile)|

## Riferimenti utili

* [[Algoritmi di ricerca non informata]]
* [[Euristica ammissibile]]