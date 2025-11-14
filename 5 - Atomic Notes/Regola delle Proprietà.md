*status*: #finito 
*tags*:  [[PDP]] [[OOP]] [[JAVA]]

## Regola delle Proprietà

> Il _sotto-tipo_ deve preservare tutte le _proprietà_ verificabili sugli oggetti del _super-tipo_.

In pratica _ogni ragionamento_ sulle proprietà degli oggetti basato sul _super-tipo_ è ancora valido quando gli oggetti appartengono al _sotto-tipo_.

È un concetto astratto, lo so, ma effettivamente è utile. Per dirlo in un terzo modo, si cerca di mantenere le caratteristiche chiave di ciò che la super-classe rappresenta. Con gli esempi diventa molto più chiaro.

**Nota**: si parla di proprietà degli **oggetti**, non dei _metodi_.

### 2 tipi di Proprietà

Le **proprietà** possono essere di due tipi: 
 1) __invarianti__:
 		proprietà sempre vere
 2) **di evoluzione**:
		proprietà che cambiano in base all'evoluzione delle circostanze

Queste proprietà sono individuate in _fase di progettazione_ e incluse nella _specifica della classe_ (in __//OVERVIEW__).

### Esempi di Proprietà degli oggetti

#### Proprietà invarianti:
* Un oggetto IntSet ha sempre elementi tutti diversi tra loro

#### Proprietà di evoluzione
* il numero di elementi di un IntSet non può diminuire nel tempo
* se una chiamata add(n) restituisce true, da quel punto in poi contains(n) restituirà sempre true (stesso n)



## Riferimenti utili

* [[Principio di Sostituzione di Liskov]]
* [[regole derivate da LSP]]