*status*: #bozza 
*tags*: [[RO]] [[Grafi e Reti di Flusso]] [[flusso massimo]] [[ESERCIZI RO]]

## Compito1-es3

![[compito1-es3.png]]

A) I -> $b = [-5 , 0, 0, 0, 5, 0, 0, 0]$
B) II -> $b = [-5 , -2, 0, 0, 5, 0, 0, 0]$
C) III -> 1 non è aumentante al passo 6,5 mentre 2 non finisce in 5 (ovvero al nodo target)
D) III -> $N_{s}=\{1\} \to 12$, $N_{s}=\{1,2\}$ -> 15
E) III -> $N_{t}=\{5\} \to 8$, $N_{t}=\{5,7,8,9\} \to 8$
F) II
**algoritmo Edmonds&Karp**:
*it. 1*: 
* viene trovato il cammino aumentante $1 \to 2 \to 5$
* può aumentare massimo di 2
* il valore del flusso aggiornato è 7, mentre il taglio è $N_{t}=\{5,7,8\}$ con valore 11 -> l'algoritmo prosegue
*it. 2*:
* viene trovato il cammino aumentante $1 \to 2 \to 6 \to 9 \to 5$
* può aumentare massimo di 1
* il valore del flusso aggiornato è 8, il taglio trovato è $N_{t}=\{5,7,8,9\}$ con valore 8. L'algoritmo si ferma.

G) II -> Vedi sopra

E) Per capire di quanto è possibile aumentare il flusso massimo da un solo nodo, partiamo studiando le capacità residue degli archi uscenti dal nodo sorgente (questo perché il valore del flusso è per forza pari al flusso in uscita dal nodo sorgente). Notiamo che per l'arco $(1,2)$ è 3, mentre per l'arco $(1,4)$ è 1. Ciò vuol dire che invertendo un qualsiasi arco del grafo in modo che formi un cammino aumentante che comprende uno dei due archi, il valore del flusso massimo non può aumentare che di 3. Notiamo però che invertendo l'arco (5,1) aumenteremmo il flusso di 5. Ciò vuol dire che è l'unico arco che invertendolo ci garantisce di star aumentando della massima quantità possibile (cioé 5) il flusso massimo.


## Riferimenti utili

* [[4.4 - Definizione - Flusso ammissibile e Valore del flusso]]