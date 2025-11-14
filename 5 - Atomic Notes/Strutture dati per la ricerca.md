*tags*: [[introAI]] [[DEFINIZIONI]] [[AGENTI BASATI SULLA RICERCA]]

## Strutture dati per la ricerca

### Nodo

- **n.STATO** – Lo stato a cui corrisponde il nodo
    
- **n.PADRE** – Il nodo nell’albero di ricerca che ha generato il nodo corrente
    
- **n.AZIONE** – L’azione applicata allo stato del padre per generare il nodo corrente
    
- **n.COSTO-CAMMINO** – Il costo totale del cammino dallo stato iniziale al nodo corrente

### Frontiera
è implementata come una coda
 * di priorità -> algoritmo best first
 * FIFO -> algoritmo in ampiezza
 * LIFO -> algoritmo in profondità

### Stati raggiunti
tabella di lookup (es. hash)
* ogni chiave è uno stato
* ogni valore è il nodo per tale stato

#### Osservazioni
* seguendo n.Padre dal nodo obiettivo ripercorro il cammino soluzione
* 
## Riferimenti utili

* 