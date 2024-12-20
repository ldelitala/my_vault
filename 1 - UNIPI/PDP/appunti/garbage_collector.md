
# Garbage Collector

## Cosa è un Garbage Collector?

Un uso scorretto della memoria può causare problemi come:
- **Memory Leak**: mancata deallocazione della memoria inutilizzata
- **Dangling Reference**: puntatori a memoria già deallocata
- **Null Pointer Dereferencing**: tentativo di accesso a un puntatore nullo
- **Heap Fragmentation**: frammentazione della memoria

La gestione manuale della memoria, però, viola il principio dell'astrazione nei linguaggi di programmazione, costringendo a operare a un livello basso. Per questo nasce il concetto di **Garbage Collector**:

> Un _sistema automatico_ di gestione della memoria che identifica e libera la memoria occupata da _oggetti non più utilizzati_, prevenendo memory leak e ottimizzando l'uso della memoria.

---

## Dove vive il Garbage Collector?

Il **Garbage Collector** non è solo un' *astrazione linguistica*!!!
Questo è infatti implementato dalle **Macchine Virtuali** (VM), che:

- Hanno accesso diretto alla memoria e alle istruzioni di allocazione/deallocazione.
- Gestiscono concretamente la memoria automatizzata, mentre il linguaggio offre solo le sintassi e le astrazioni (come classi e riferimenti).

La **VM** quindi implementa il garbage collector come parte integrante della sua architettura, rendendo la gestione automatica della memoria un elemento concreto, non solo teorico.

## Il Garbage Collector Perfetto
![[garbage_collector_perfetto.jpg]]

Il garbage collector ideale dovrebbe possedere le seguenti caratteristiche:

* **Nessun impatto visibile sulle performance dei programmi:**  
    Deve funzionare in modo da non influire sulla velocità di esecuzione, rimanendo invisibile all'utente.

* **Compatibilità universale:**  
    Capace di operare su qualsiasi programma e struttura dati dinamica, comprese le strutture cicliche (che rappresentano una sfida tipica per i garbage collector).

* **Identificazione precisa del garbage:**  
    Rileva e rimuove solo la memoria non più utilizzata, evitando errori e mantenendo elevata l'efficienza.

* **Assenza di overhead di memoria:**  
    Non introduce costi aggiuntivi nella gestione complessiva della memoria.

* **Gestione ottimizzata dell'heap:**  
    Consente un uso efficace e organizzato dell'heap, migliorando le prestazioni e riducendo la frammentazione.

## Reference Counting

In poche parole, ogni blocco di memoria allocato ha un contatore che tiene traccia del numero di riferimenti a quel blocco. Ogni volta che viene aggiunto o rimosso un riferimento, il contatore si aggiorna. Quando il contatore arriva a zero, la memoria viene liberata automaticamente.

### Pro

* **Incrementale:**  
    La gestione della memoria avviene progressivamente e distribuita nel tempo, senza necessità di pause o scansioni complete della memoria (come invece accade con altri sistemi di garbage collection).

* **Semplice da implementare:**  
    Il reference counting richiede poco codice per essere integrato ed è abbastanza intuitivo.

* **Compatibile con la gestione esplicita della memoria:**  
    Può convivere con metodi di gestione esplicita della memoria, come `malloc` e `free`.

* **Riuso immediato della memoria libera:**  
    Quando l'ultimo riferimento viene eliminato, il contatore scende a zero e la memoria viene liberata istantaneamente, rendendo le celle libere subito disponibili.

### Contro

* **Incrementale:**  
    L'aggiornamento dei contatori avviene ad ogni operazione sui riferimenti, aumentando il tempo di esecuzione in proporzione alla complessità del codice.  
    _In alcuni casi, questa soluzione risulta meno efficiente, poiché altre tecniche di garbage collection raccolgono la memoria solo periodicamente, permettendo un'esecuzione ininterrotta tra un aggiornamento e l’altro._

* **Richiede spazio aggiuntivo in memoria:**  
    Per ogni blocco di memoria allocato è necessario memorizzare anche un contatore.

* **Problemi con strutture dati cicliche:**  
    Non può gestire correttamente strutture dati che contengono cicli interni, poiché i contatori non arrivano mai a zero.  Ad esempio:
    
    ![[cicli_interni.png]]

## Mark & Sweep

Nel metodo **Mark & Sweep**, ogni cella di memoria contiene un bit di marcatura. Quando l’heap è quasi pieno, il garbage collector sospende l’esecuzione del programma per effettuare una pulizia in due fasi:

1. **Marking**  
    Partendo dal *root set*, il garbage collector marca tutte le celle attivamente in uso.

2. **Sweep**  
    - Le celle non marcate vengono identificate come garbage e aggiunte alla lista di celle libere.
    - Il bit di marcatura delle celle attive viene resettato, preparandole per il prossimo ciclo.

### Glossario
- **Cella:** blocco di memoria nell'heap.
- **Root set:** insieme dei dati attivi, che comprende le variabili statiche e quelle allocate sul run-time stack.

![[root_set.png]]

### Pro

* Efficace nel gestire strutture circolari senza perdite di memoria.
* Non richiede spazio aggiuntivo significativo.

### Contro

* **Sospensione dell’esecuzione:** il programma si interrompe durante la fase di pulizia.
* **Frammentazione della memoria:** le celle attive possono trovarsi sparse, riducendo la compattezza.
* **Tempo di esecuzione elevato:** proporzionale alla dimensione complessiva dell’heap.
* **Bassa località dei dati:** nel tempo, dati di età diverse finiscono per essere vicini, peggiorando le prestazioni.

## Copying Collection

Il **Copying Collection** è un metodo semplice e intuitivo per la gestione della memoria. Funziona suddividendo l’heap in due sezioni: *from-space* e *to-space*. Durante l’esecuzione, solo una delle due è attiva e viene usata per allocare nuove celle.

Quando la memoria della sezione attiva si riempie quasi del tutto, il garbage collector viene attivato. A questo punto, le celle ancora in uso (*celle live*) vengono copiate nell'altra metà dell'heap in modo compatto. Alla fine del processo, i ruoli di *from-space* e *to-space* si scambiano, e la nuova sezione attiva è pronta per ulteriori allocazioni.

Per la copia delle celle si utilizza l’**Algoritmo di Cheney**, che organizza e compatta i dati in modo efficiente.

### Pro

* **Evita problemi di frammentazione:**  
    Compatta la memoria a ogni raccolta, mantenendo un’allocazione continua e ordinata.

### Contro

* **Duplicazione dello spazio heap:**  
    Richiede il doppio della memoria, il che può essere problematico su dispositivi con risorse limitate.  
    _Funziona meglio su architetture a 64-bit, dove l’abbondanza di memoria compensa la duplicazione._


## Generational Garbage Collection

L’idea alla base del **Generational Garbage Collection** è che alcuni blocchi di memoria hanno una vita molto breve, mentre altri durano più a lungo. Per esempio, le variabili locali di una funzione, che esistono solo per la durata di un blocco di codice, tendono a essere eliminate rapidamente. 

Per ottimizzare la gestione della memoria, l’heap viene suddiviso in "generazioni", ciascuna corrispondente a una diversa età dei blocchi. Le generazioni più giovani, che contengono blocchi a vita breve, ricevono meno spazio ma vengono pulite frequentemente. Le generazioni più vecchie, dove si trovano blocchi più longevi, ricevono più spazio e vengono pulite meno spesso.

Il caso più semplice prevede due generazioni:
1. **Young Generation:** è l’area per le nuove allocazioni. Quando questa si riempie, il garbage collector copia i blocchi ancora vivi nella generazione successiva, **Old Generation**.
2. **Old Generation:** è l’area per i blocchi più duraturi. Poiché i riferimenti qui decrescono meno frequentemente, viene pulita solo occasionalmente.

Dopo la copia dei blocchi vivi da Young a Old:
1. **Young** viene ripulita, pronta per nuove allocazioni.
2. **Old** può essere pulita con qualsiasi metodo di garbage collection, in base alle necessità.

Questa struttura riduce il numero di operazioni di pulizia per i blocchi a vita lunga e mantiene più efficiente la gestione della memoria.

**PS** notare come sia lo stesso concetto delle gerarchie di memoria ma con l'heap 
