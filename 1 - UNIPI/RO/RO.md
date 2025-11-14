*status*: #finito 
*tags*: [[UNIPI]]

**Professore**: Antonio Frangioni
**CFU**: 6 cfu

## Argomenti principali

* [ ] [[PROGRAMMAZIONE LINEARE]]
	* [ ] [[DUALITÀ]]

## Raccolte utili

* [[DEFINIZIONI MATEMATICHE PURE RO]]
* [[TEOREMI]]
* [[ALGORITMI]]
* [[ESERCIZI RO]]

## Sotto - argomenti

### Problemi e Modelli

* [ ] [[1 - Definizione - Algoritmo esatto vs Algoritmo euristico]] !!!
* [ ] [[Definizione - Variabili quantitative, Variabili Logiche o Proposizionali, Variabile a valori discreti]]
	* [ ] [[Relazioni tra variabili proposizionali]] !!! Impportante per scritto, orale penso chill
* [ ] [[Definizione - Variabili di assegnamento vs Variabili di semi-assegnamento]]
* [ ] [[Definizione - Problema di copertura, Problema di Partizione, Problema di Riempimento]] !!!
* [ ] [[Definizione - vincoli disgiuntivi]]


### Grafi e Reti di flusso

#### Albero dei cammini minimi
* [x] [[1 - Introduzione - Problema dell'albero dei cammini minimi]]
	* [x] [[1.1 - Definizione - Problema SP]] !
	* [x] [[1.2 - Definizione - Problema SPT]] !!!
	* [x] [[1.3 - Algoritmo - SPT Shortest Path Tree]] !!!!
		* [x] [[1.3.1 - Algoritmo - SPT.S Shortest Path Tree Shortest-First]] !!!!
		* [x] [[1.3.2 - Teorema - Proprietà di SPT.S con cicli non negativi]]
		* [x] [[1.3.3 - Algoritmo - SPT.L]] !!!!
			* [x] [[1.3.3.1 - Algoritmo - Algoritmo di Bellman]] !!!
	* [x] [[1.4 - Problema e soluzione dei cammini minimi con più radici]] !!
#### Albero di copertura di costo minimo
* [x] [[2 - Introduzione - Problema dell'albero di copertura di costo minimo]]
	* [x] [[2.1 - Definizione - Problema dell'albero di copertura di costo minimo (MST)]] !!!
	* [x] [[2.2 - Differenza tra l'albero di copertura di costo minimo e quello dei cammini minimi]]
	* [x] [[2.3 - Algoritmo - Greedy MST]] !!!!
		* [x] [[2.3.1 - Algoritmo - Algoritmo di Kruskal]] !!!!
		* [x] [[2.3.2 - Algoritmo - Algoritmo di Prim]] !!!!

#### Flusso massimo
* [x] [[3 - Definizione - Problema del flusso massimo]] !!!
	* [x] [[3.1 - Teorema - Taglio minimo uguale a Flusso Massimo]] !!!!
	* [x] [[3.2 - Algoritmo - Cammini Aumentanti]] !!!!
		* [x] [[3.2.1 - Algortimo - Edmonds & Karp]] !!!!
		* [x] [[3.2.2 - Problema del flusso massimo con più sorgenti e pozzi]] !!!

#### Flusso di costo minimo
* [x] [[4 - Definizione - Problema del flusso di costo minimo]] !!!!
	* [x] [[4.1 - Definizione - rete e deficit]] !
	* [x] [[4.2 - Definizione - Domanda Globale e Offerta Globale]] !
	* [x] [[4.3 - Definizione - Vincoli di Conservazione del Flusso e Vincoli di capacità sugli archi]] !!!!
	* [x] [[4.4 - Definizione - Flusso ammissibile e Valore del flusso]] !!!!
	* [x] [[4.5 - Definizione - Pseudoflusso]] !!!!
	* [x] [[4.6 - Definizione - Sbilanciamento, eccesso di flusso e difetto di flusso, nodo bilanciato]] !!!!
	* [x] [[4.7 - Definizione - Pseudoflusso minimale]] !!!!!
		* [x] [[4.7.1 - Corollario - Pseudoflusso minimale se non esistono cicli aumentanti]]
	* [ ] [[4.8 - Operazioni di modifica dello pseudoflusso]]
	* [ ] [[4.9 - Algoritmo - Cancella Cicli]] !!!!!
	* [ ] [[4.10 - Algoritmo - cammini minimi successivi]] !!!!!

### PROGRAMMAZIONE LINEARE

#### definizioni degli elementi grafici del problema
* [ ] [[1 - Sottospazio Lineare e Sottospazion Affine]]
* [ ] [[2 - Iperpiano]]
* [ ] [[3 - Semispazio]]
* [ ] [[4 - Poliedro]]
* [ ] [[5 - Insieme Convesso]]

* [ ] [[7 - Cono]]
	* [ ] [[7.1 - Cono Convesso Poliedrico]]

* [ ] [[8 - Direzione di Recessione di un Poliedro]]
	* [ ] [[8.1 - le direzioni di recessione di un poliedro formano un cono]]

* [ ] [[9 - Inviluppo]]
* [ ] [[9.1 - Inviluppo Conico]]
* [ ] [[9.2 - Inviluppo Convesso]]
* [ ] [[10 - Faccia di un Poliedro]]
	* [ ] [[10.1 - Proprietà delle facce di un Poliedro]]
	* [ ] [[10.2 - Faccia massimale e Faccia minimale]]

#### Programmazione Lineare
##### Introduzione all'argomento
* [x] [[1 - Definizione - Problema di Programmazione Lineare]] !!!!
	* [x] [[1.1 - Modello Standard di PL]] !
		* [x] [[1.1.1 - tecniche di standardizzazione dei problemi di PL]]

##### Le basi: gli strumenti per capire il problema

* [x] [[2 - Teorema - il cono delle direzioni di recessione]] !!!
	* [x] [[2.1 - Corollario - Linealità di P]] !!

* [x] [[3 - Teorema - condizione di illimitatezza superiore al problema di PL]]

* [x] [[4 - Teorema - qualsiasi cono finitamente generato è un cono poliedrico, e viceversa]]
	* [x] [[4.1 - Lemma - relazione bidirezionale tra vettori del cono e i suoi generatori]]

* [x] [[5 - Teorema - un poliedro è la somma di un inviluppo conico e un inviluppo convesso]] !
	* [ ] [[5.1 - Corollario - condizione necessaria e sufficiente della soluzione ottima del problema di PL]]
		* [ ] [[5.1.1 - Nota - Riflessioni sul corollario]]

* [ ] [[6 - Teorema - Riduzione di variabili in un problema di PL con linealità]]
	* [ ] [[6.1 - Dimostrazione - Riduzione di variabili in un problema di PL con linealità]]
	* [ ] [[6.2 - Esempio - Riduzione di variabili in un problema di PL con linealità]]
	* [ ] [[6.3 - Corollario - Proprietà del problema ridotto]]
		* [ ] [[6.3.1 - Dimostrazione - Proprietà del problema ridotto]]

##### avanzato: strumenti per risolvere il problema algebricamente
* [x] [[7 - Definizione - insieme degli indici dei vincoli attivi]] !!
* [x] [[8 - Definizione - direzione ammissibile]] !!!!
	* [ ] [[8.1 - Proprietà - una direzione è ammissibile se appartiene al cono degli indici attivi]]
* [x] [[9 - Definizione - Base di un Poliedro]] (!!!! importantissimo)
	* [x] [[9.1 - Corollario - punto estremo di un Poliedro]] !
	* [x] [[9.2 - Definizione - Cono di recessione associato ad una base]]
	* [ ] [[9.2.1 - Tecnica per trovare i vettori generatori di un cono di recessione associato ad una base]]

#### Teoria della Dualità

##### Le basi: teoria sulla dualità
* [x] [[1 - Introduzione - Teoria della Dualità]]
	* [x] [[1.1 - Definizione - il Problema Duale associato]] !!!!!

* [x] [[2 - Teorema - il Duale del Duale è il Primale]] !!!

* [x] [[3 - Teorema - dualità debole]] !!!!!!
	* [x] [[3.1 - Corollario - Se il primale è illimitato il Duale è vuoto]] !!
	* [x] [[3.2 - Corollario - certificato di ottimalità]] !!!

* [x] [[4 - Teorema - dualità forte]] !!!!!!
	* [x] [[4.1 - Teorema - relazione tra soluzioni del primale e duale]] !!!

##### avanzato: algebra della dualità
* [x] [[5 - Teorema - soluzioni e scarti complementari]] !!!!
	* [x] [[5.1 - Definizione - Soluzioni complementari e Scarti Complemetari]] !!!!
	* [x] [[5.2 - Proposizione - condizione necessaria e sufficiente per la ottimalità della soluzione]] !!!!
	* [x] [[5.3 - Esempio - Applicazione del Teorema degli scarti complementari]]
	* [x] [[5.4 - Corollario - Estensione del teorema sulla relazione tra soluzioni e scarti complementari]] !
	* [x] [[5.5 - Esempio - Applicazione del corollario che estende il Teorema degli scarti complementari]]

* [x] [[6 - Teorema - condizione necessaria e sufficiente per la ottimalità della soluzione]] !!!
	* [x] [[6.1 - Definizione - Insieme complementare alla Base]] !!!!
	* [x] [[6.2 -  Definizione - Soluzione Duale associata alla Base]] !!!!
	* [x] [[6.3 - Tabella delle soluzioni di base complementari]] !!!!!

#### Algoritmi del Simplesso
* [x] [[1 -  Introduzione - Algoritmo del Simplesso Primale ]]
	* [x] [[1.1 - L'albero dei casi dell'algorimto del Simplesso Primale]]
		* [x] [[1.1.1 - Verificare se ci siano o meno direzioni di crescita]]
			* [x] [[1.1.1.a - Esempio pratico su come verificare se ci siano o meno direzioni di crescita]]
	* [x] [[1.2 - Algoritmo - Algoritmo algebrico del Simplesso Primale]] !!!!
	* [x] [[1.3 - Algoritmo - Algoritmo geometrico del Simplesso Primale]] !!!!

* [x] [[2 - Algoritmo - Algoritmo algebrico del Simplesso Duale]] !!!!
	* [x] [[2.1 - Algoritmo - Algoritmo geometrico del Simplesso Duale]] !!!

### Programmazione Lineare Intera

* [x] [[1 - Definizione - Problema di Programmazione Lineare Intera (PLI)]] (!!!!!)
	* [x] [[1.1 - Definizione - Problema di Programmazione Lineare Mista (PLM)]] (!)
	* [x] [[1.2 - Definizione - Rilassamento continuo della PLI]] (!!!!)

* [x] [[2 - Introduzione - Algoritmo Branch & Bound (B&B)]]
	* [x] [[2.1 - Algoritmo - Branch & Bound (B&B)]] !!!!!!
	* [x] [[2.2 - Caratteristiche richieste al metodo di Branching perfetto]] (!!)
	* [x] [[2.3 - Introduzione - B&B applicato al Problema dello Zaino]] (!)
	* [x] [[2.4 - Algoritmo - B&B applicato al Problema dello Zaino]] (!!!!!)
	* [x] [[2.3 - Algoritmo - B&B applicato al Problema del Commesso Viaggiatore (TSP)]] (!!!!!!)

## Definizioni
### Grafi e Reti di Flusso

#### Cosa è un Flusso
* [ ] [[4.1 - Definizione - rete e deficit|rete e deficit]]
* [ ] [[4.3 - Definizione - Vincoli di Conservazione del Flusso e Vincoli di capacità sugli archi|Vincoli di Conservazione del Flusso e Vincoli di capacità sugli archi]]
* [ ] [[4.4 - Definizione - Flusso ammissibile e Valore del flusso|Flusso ammissibile e Valore del flusso]]
* [ ] [[4.5 - Definizione - Pseudoflusso|Pseudoflusso]]
* [ ] [[4.6 - Definizione - Sbilanciamento, eccesso di flusso e difetto di flusso, nodo bilanciato|Sbilanciamento, eccesso di flusso e difetto di flusso, nodo bilanciato]]

#### Problema dell'albero dei cammini minimi SPT
* [[1.1 - Definizione - Problema SP|Problema SP]]
* [[1.2 - Definizione - Problema SPT|Problema SPT]]

#### Problema dell'albero di copertura di costo minimo MST
* [ ] [[2.1 - Definizione - Problema dell'albero di copertura di costo minimo (MST)|Problema MST]]


* [ ] [[3 - Definizione - Problema del flusso massimo|Problema del flusso massimo]]
* [ ] [[4 - Definizione - Problema del flusso di costo minimo|Problema del flusso di costo minimo]]

### Programmazione Lineare
* [ ] [[1 - Definizione - Problema di Programmazione Lineare|Problema di Programmazione Lineare]]
* [ ] [[1.1 - Definizione - il Problema Duale associato|il Problema Duale associato]]
* [ ] [[9 - Definizione - Base di un Poliedro|Base di un Poliedro]]
* [ ] [[6.1 - Definizione - Insieme complementare alla Base|Insieme complementare alla Base]]
* [ ] [[6.2 -  Definizione - Soluzione Duale associata alla Base|Soluzione Duale associata alla Base]]
* [ ] [[5.1 - Definizione - Soluzioni complementari e Scarti Complemetari|Soluzioni complementari e Scarti Complemetari]]

### Programmazione Lineare Intera
* [ ] [[1 - Definizione - Problema di Programmazione Lineare]]
	* [ ] [[1.1 - Definizione - Problema di Programmazione Lineare Mista (PLM)]]

